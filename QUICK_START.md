# Quick Start Guide - GST Return Filing Tracker

## 30-Second Setup

```bash
pnpm install
pnpm dev
# Open http://localhost:3000
```

That's it! The app is ready with sample data.

## What You Can Do Right Now

### 1. **View Dashboard** (Default Tab)
- See 5 clients with their filing status
- Track 3 overdue returns
- View ₹500 in penalties
- Check recent activity

### 2. **Manage Clients** (Clients Tab)
- Browse all 5 sample clients
- Search by name or GSTIN
- See GSTR1 and GSTR3B status for each
- View penalties and last sync dates
- Click the arrow icon to view client details

### 3. **Export Data** (Top Right Button)
- Click "Export Reports" to download all client data as CSV
- Click client detail's "Export Report" for individual CSV
- Open in Excel or Google Sheets

### 4. **View Notifications** (Notifications Tab)
- See 1 unread reminder notification
- Filter between all/unread
- Mark as read or delete
- See notification details

### 5. **View Client Details**
- Click arrow on any client row
- See complete client information
- View all GSTR1/GSTR3B details
- Check due dates and penalties
- Send reminder or export report

## Sample Data Breakdown

### Clients (5 total)
1. **ABC Trading** - GSTR1 filed, GSTR3B pending
2. **XYZ Manufacturing** - GSTR1 delayed (₹500 penalty), GSTR3B pending
3. **Tech Solutions** - Both GSTR1 & GSTR3B filed ✓
4. **Retail Ventures** - GSTR1 filed, GSTR3B pending
5. **Global Exports** - GSTR1 amended, GSTR3B filed

### Filing Status
- **5** Returns filed
- **0** Due soon (pending)
- **3** Overdue
- **₹500** In penalties

## Tab Navigation

| Tab | Purpose | What You'll See |
|-----|---------|-----------------|
| **Dashboard** | Overview | Metrics, recent activity feed |
| **Clients** | Management | Searchable client list with status |
| **Notifications** | Alerts | Filing reminders and alerts |

## Key Features to Try

### Search Clients
- Go to Clients tab
- Type in the search box
- Filter by name (e.g., "ABC") or GSTIN

### View Client Details
- Click the arrow (→) button on any client
- See complete information
- View filing status for each return type
- Check penalties

### Export Client Report
- Open client details (arrow button)
- Click "Export Report" button
- CSV file downloads with timestamp

### Export All Reports
- Click "Export Reports" button in top right
- All client data exports as single CSV
- Perfect for sending to stakeholders

### Send Reminder
- Open client details
- Click "Send Reminder" button
- Simulated email sent to client
- Notification appears in Notifications tab

### Manage Notifications
- Go to Notifications tab
- See unread count (red badge)
- Filter "All" vs "Unread"
- Click checkmark to mark as read
- Click X to delete

## File Statuses Explained

- **FILED** ✓ - Return submitted on time
- **AMENDED** 🔄 - Return was amended after filing
- **NOT_FILED** ⏳ - Return pending (due soon)
- **DELAYED** ⚠️ - Filed late (penalty applied)

## Penalty Calculation

Each overdue filing incurs penalty:
- First 100 days: **₹20/day**
- After 100 days: **₹50/day**

Example: If a return is 15 days late = ₹300 penalty

## API Endpoints Available

### Export API
```
POST /api/export
Body: { reportType: "all" }
Returns: XLSX file
```

### Email Notification API
```
POST /api/notifications/email
Body: { clientId: "string", type: "REMINDER" | "ALERT" }
Returns: { success: true, message: "..." }
```

## Color Coding Quick Reference

| Color | Meaning |
|-------|---------|
| 🟢 Green | FILED - Complete |
| 🔵 Blue | AMENDED - Updated |
| 🟡 Yellow | NOT_FILED - Pending |
| 🔴 Red | DELAYED - Overdue |

## Common Tasks

### I want to see client details
1. Go to "Clients" tab
2. Click the arrow button on any row
3. Modal pops up with all info

### I want to send a reminder email
1. Click arrow on client
2. Click "Send Reminder" button
3. Confirmation appears
4. See notification in Notifications tab

### I want to export everything
1. Click "Export Reports" button (top right)
2. CSV file downloads automatically
3. Open in Excel/Sheets

### I want to find a specific client
1. Go to "Clients" tab
2. Type in search box
3. Results filter in real-time

### I want to check what's overdue
1. Go to "Dashboard" tab
2. Look for "Overdue Returns: 3"
3. Check "Overdue Returns" card
4. View details in Clients tab

## Real-World Usage

### For CA Practice
- Daily: Check dashboard for overdue filings
- Weekly: Export reports for client meetings
- Monthly: Monitor penalties and trends
- Quarterly: Generate compliance reports

### For Team
- Assign clients to team members
- Track individual performance
- Monitor deadline compliance
- Generate team statistics

### For Clients
- Send reminders before deadlines
- Provide filing status updates
- Export compliance certificates
- Show penalty avoidance

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Tab` | Navigate between elements |
| `Enter` | Click focused button |
| `Esc` | Close modal |
| `Ctrl+F` | Search page (browser) |

## Mobile Experience

The app works perfectly on mobile:
- Responsive design adapts to screen size
- All features available
- Touch-friendly buttons
- Optimized for small screens

## Troubleshooting

### App not loading?
- Ensure you ran `pnpm dev`
- Check `http://localhost:3000`
- Look for port 3000 in terminal

### Search not working?
- Type full or partial name
- Try GSTIN number
- Case-insensitive search works

### Export not downloading?
- Check browser's download folder
- Check pop-up blocker settings
- Try in different browser

### Notifications not showing?
- Go to Notifications tab
- Click filter buttons
- Check unread count

## Next Steps

1. **Explore the data** - Spend 5 minutes clicking around
2. **Try the search** - Find clients by name or GSTIN
3. **Export reports** - Download sample data
4. **Send reminder** - See notifications in action
5. **Read documentation** - Check README.md for details

## Customization

The app uses mock data. To connect real data:
- Replace `/lib/mockData.ts` with database queries
- Update `/app/page.tsx` to fetch from API
- Connect to real GST Portal

## Support

- **Documentation**: See README.md
- **Implementation Details**: See IMPLEMENTATION.md
- **Code Comments**: Throughout source files
- **Types**: TypeScript interfaces in `/lib/types.ts`

## Version Info

- **App**: v1.0.0
- **Next.js**: 16.2.6
- **React**: 19
- **Node**: 18+
- **Package Manager**: pnpm 10+

---

**Start exploring now!** 🚀

Open http://localhost:3000 and navigate the GST Filing Tracker.
