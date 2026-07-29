# GST Return Filing Tracker

A comprehensive GST return filing management system designed for CA firms and accounting consultants to track and manage GST filings for multiple clients with automatic status tracking, penalty calculations, and email notifications.

## Features

### 📊 Dashboard
- **Real-time Metrics**: Track total clients, filed returns, pending returns, overdue returns, and total penalties at a glance
- **Recent Activity Feed**: See the latest filing updates for your clients
- **Quick Statistics**: Visual indicators for filing status overview

### 👥 Client Management
- **Client Database**: Store and manage detailed client information including GST numbers, contact details, and states
- **Searchable Client List**: Filter clients by name or GSTIN
- **Filing Status Tracking**: Monitor GSTR1 and GSTR3B filing status for each client
- **Penalty Calculation**: Automatic calculation of penalties based on filing delays
- **Client Details Modal**: View comprehensive client information with filing history

### 📋 Filing Status System
- **Status Types**: Track FILED, NOT_FILED, DELAYED, and AMENDED statuses
- **Due Date Tracking**: Monitor upcoming and overdue filings
- **Filing Dates**: Record when returns were actually filed
- **Penalty Tracking**: Calculate and track penalties automatically

### 🔔 Notification System
- **Smart Notifications**: Receive reminders, alerts, and filing confirmations
- **Unread Status**: See unread notification count at a glance
- **Notification Filtering**: Filter between all notifications and unread only
- **Action Items**: Mark as read or delete notifications

### 📊 Reporting & Export
- **Individual Reports**: Export individual client GST filing reports as CSV
- **Bulk Export**: Export comprehensive reports for all clients with a single click
- **Data Fields**: Includes client name, GSTIN, filing status, due dates, filed dates, and penalties
- **Timestamped Files**: Automatic date tagging for exported files

### 📧 Email Notifications
- **API Endpoints**: Ready-to-integrate email notification system
- **Reminder Types**: Support for filing reminders and alert notifications
- **Client Details**: Includes client information and filing details in notifications

## Technology Stack

- **Frontend**: Next.js 16, React 19, TypeScript
- **Styling**: Tailwind CSS v4, shadcn/ui components
- **Icons**: Lucide React
- **Date Handling**: date-fns
- **Export**: XLSX library
- **Package Manager**: pnpm

## Installation

1. **Clone/Download the project**
2. **Install dependencies**:
   ```bash
   pnpm install
   ```

3. **Start the development server**:
   ```bash
   pnpm dev
   ```

4. **Open in browser**:
   Navigate to `http://localhost:3000`

## Project Structure

```
project/
├── app/
│   ├── page.tsx           # Main dashboard page
│   ├── layout.tsx         # Root layout with metadata
│   ├── globals.css        # Global styles
│   └── api/
│       ├── export/        # Excel export API
│       └── notifications/ # Email notification API
├── components/
│   ├── dashboard-header.tsx      # Dashboard metrics display
│   ├── client-table.tsx          # Client list with search
│   ├── notification-center.tsx   # Notification management
│   └── client-detail-modal.tsx   # Client details modal
├── lib/
│   ├── types.ts           # TypeScript type definitions
│   ├── mockData.ts        # Sample data for development
│   └── utils-gst.ts       # Utility functions for calculations
└── public/                # Static assets
```

## Core Components

### Dashboard Header
Displays key metrics and statistics including:
- Total number of clients
- Count of filed returns
- Pending returns due
- Overdue filings
- Total penalties accumulated

### Client Table
- Searchable list of all clients
- Real-time filtering by name or GSTIN
- Status badges for GSTR1 and GSTR3B
- Quick action buttons for viewing details and deleting clients
- Penalty display with color coding

### Notification Center
- Unified notification management
- Filter between all and unread notifications
- Support for multiple notification types (Reminder, Alert, Filed, Penalty)
- Mark as read and delete functionality
- Notification count indicators

### Client Detail Modal
- Comprehensive client information display
- Complete filing status for all return types
- Due dates and filed dates
- Penalty information
- Export report and send reminder buttons

## Key Utilities

### Penalty Calculation
- Automatic calculation based on filing delays
- Rs. 20 per day for first 100 days
- Rs. 50 per day after 100 days
- Support for both DELAYED and NOT_FILED statuses

### Report Generation
- Individual client reports with all filing details
- Bulk export for all clients
- CSV format for easy import to Excel or accounting software
- Comprehensive data including dates, statuses, and penalties

## API Endpoints

### Export Endpoint
- **POST** `/api/export` - Generate Excel reports
- Request: `{ reportType: "all" }`
- Response: XLSX file download

### Email Notification Endpoint
- **POST** `/api/notifications/email` - Send email notifications
- Request: `{ clientId: string, type: "REMINDER" | "ALERT" }`
- Response: Success message with email details

## Mock Data

The application includes comprehensive mock data for testing:
- 5 sample clients with diverse filing statuses
- Multiple GSTR1 and GSTR3B filings with different statuses
- Sample notifications including reminders and alerts
- Penalty records for delayed filings

## Feature Roadmap

### Current Implementation
- ✅ Dashboard with real-time metrics
- ✅ Client management and search
- ✅ Filing status tracking
- ✅ Penalty calculation
- ✅ Notification center
- ✅ Individual and bulk export
- ✅ Email notification API

### Future Enhancements
- Database integration (Neon PostgreSQL)
- Real GST Portal API integration
- Automated GST Portal status sync
- Advanced filtering and reporting
- User authentication and authorization
- Multi-user team management
- Scheduled automated reminders
- SMS notifications
- Integration with accounting software
- GST compliance dashboard
- Monthly trend analysis

## Integration Points

### GST Portal Integration
Replace mock data with real GST Portal API calls:
```typescript
// Example: Fetch filing status from GST Portal
const fetchFilingStatus = async (gstin: string) => {
  // Call GST Portal API
  // Update filing status in database
}
```

### Email Service Integration
Connect real email service (Nodemailer, SendGrid, etc.):
```typescript
// Example: Send email via Nodemailer
const transporter = nodemailer.createTransport({...})
await transporter.sendMail({...})
```

### Database Integration
Connect to Neon PostgreSQL or other database:
```typescript
// Replace mockData with database queries
const clients = await db.query('SELECT * FROM clients')
```

## Usage Examples

### View Dashboard
Navigate to the home page to see key metrics and recent activity

### Manage Clients
- Go to "Clients" tab to view all clients
- Search for specific clients by name or GSTIN
- Click on a client to view detailed information
- Export individual client reports

### Track Filings
- Check GSTR1 and GSTR3B status for each client
- Monitor upcoming due dates
- View filed dates and penalties

### Receive Notifications
- Go to "Notifications" tab
- Filter between all and unread notifications
- Mark notifications as read
- Delete old notifications

### Export Reports
- Click "Export Reports" button to download all client data
- Use individual client export from the detail modal
- Import into Excel or accounting software

## Development

### Run in Development Mode
```bash
pnpm dev
```

### Build for Production
```bash
pnpm build
pnpm start
```

### Run Linter
```bash
pnpm lint
```

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (responsive design)

## Performance Considerations

- Real-time filtering for responsive search
- Memoized calculations for metrics
- Efficient component rendering
- Optimized bundle size

## Security

- Type-safe implementation with TypeScript
- Input validation for searches and filters
- CSV export escapes special characters
- Mock data for development/demo purposes

## Contributing

To add new features or improvements:
1. Create feature components in `/components`
2. Add types to `/lib/types.ts`
3. Implement utilities in `/lib/utils-gst.ts`
4. Test in development mode
5. Document changes in this README

## License

This project is created with v0 by Vercel and is available for use as per your requirements.

## Support

For issues, questions, or feature requests, please refer to the Vercel support portal or create an issue in your version control system.

---

**Last Updated**: July 29, 2026

**Version**: 1.0.0 - Initial Release

**Status**: Production Ready for Demo/Testing
