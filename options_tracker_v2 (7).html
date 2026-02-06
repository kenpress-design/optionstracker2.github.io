<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Options Trading Tracker</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;
            background: #f5f5f7;
            padding: 10px;
            font-size: 14px;
        }

        .container {
            max-width: 100%;
            margin: 0 auto;
            background: white;
            border-radius: 12px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 20px;
            text-align: center;
        }

        .header h1 {
            font-size: 24px;
            margin-bottom: 5px;
        }

        .header p {
            font-size: 14px;
            opacity: 0.9;
        }

        .api-setup {
            background: #fff3cd;
            border: 1px solid #ffc107;
            padding: 15px;
            margin: 15px;
            border-radius: 8px;
        }

        .api-setup input {
            width: 100%;
            padding: 10px;
            margin-top: 10px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 14px;
        }

        .controls {
            padding: 15px;
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            border-bottom: 1px solid #e0e0e0;
        }

        button {
            padding: 10px 20px;
            border: none;
            border-radius: 6px;
            font-size: 14px;
            cursor: pointer;
            transition: all 0.2s;
        }

        button:disabled {
            opacity: 0.5;
            cursor: not-allowed;
        }

        .btn-primary {
            background: #667eea;
            color: white;
        }

        .btn-primary:hover:not(:disabled) {
            background: #5568d3;
        }

        .btn-success {
            background: #10b981;
            color: white;
        }

        .btn-success:hover {
            background: #059669;
        }

        .btn-secondary {
            background: #6b7280;
            color: white;
        }

        .btn-secondary:hover {
            background: #4b5563;
        }

        .summary {
            padding: 15px;
            background: #f9fafb;
            border-bottom: 1px solid #e0e0e0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
        }

        .summary-item {
            text-align: center;
        }

        .summary-label {
            font-size: 12px;
            color: #6b7280;
            margin-bottom: 5px;
        }

        .summary-value {
            font-size: 20px;
            font-weight: bold;
            color: #111827;
        }

        .table-container {
            overflow-x: auto;
            padding: 15px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
        }

        th {
            background: #f3f4f6;
            padding: 10px 6px;
            text-align: left;
            font-size: 11px;
            font-weight: 600;
            color: #374151;
            border-bottom: 2px solid #e5e7eb;
            white-space: nowrap;
        }

        th:nth-child(2) { /* Direction */
            min-width: 65px;
        }

        th:nth-child(5) { /* Strike */
            min-width: 70px;
        }

        td {
            padding: 8px 6px;
            border-bottom: 1px solid #e5e7eb;
            font-size: 12px;
        }

        td:nth-child(2) { /* Direction */
            min-width: 65px;
        }

        td:nth-child(5) { /* Strike */
            min-width: 70px;
        }

        input[type="text"],
        input[type="date"],
        input[type="number"],
        select {
            width: 100%;
            padding: 4px;
            border: 1px solid #d1d5db;
            border-radius: 4px;
            font-size: 12px;
        }

        input:focus, select:focus {
            outline: none;
            border-color: #667eea;
        }

        .negative {
            color: #dc2626;
            font-weight: 600;
        }

        .positive {
            color: #10b981;
            font-weight: 600;
        }

        .status {
            padding: 10px;
            margin: 15px;
            border-radius: 6px;
            font-size: 13px;
        }

        .status-info {
            background: #dbeafe;
            color: #1e40af;
        }

        .status-error {
            background: #fee2e2;
            color: #991b1b;
        }

        .status-success {
            background: #d1fae5;
            color: #065f46;
        }

        .status-warning {
            background: #fef3c7;
            color: #92400e;
        }

        .btn-delete {
            background: #ef4444;
            color: white;
            padding: 4px 8px;
            font-size: 12px;
        }

        .btn-delete:hover {
            background: #dc2626;
        }

        .progress-bar {
            width: 100%;
            height: 4px;
            background: #e5e7eb;
            margin: 15px;
            border-radius: 2px;
            overflow: hidden;
            display: none;
        }

        .progress-bar.active {
            display: block;
        }

        .progress-fill {
            height: 100%;
            background: #667eea;
            width: 0%;
            transition: width 0.3s;
        }

        .debug-log {
            background: #f9fafb;
            border: 1px solid #e5e7eb;
            padding: 10px;
            margin: 15px;
            border-radius: 6px;
            max-height: 200px;
            overflow-y: auto;
            font-family: monospace;
            font-size: 11px;
            display: none;
        }

        .debug-log.active {
            display: block;
        }

        .debug-log div {
            padding: 2px 0;
            border-bottom: 1px solid #e5e7eb;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 20px;
            }
            
            .summary {
                grid-template-columns: repeat(2, 1fr);
            }

            .controls {
                flex-direction: column;
            }

            button {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>📊 Options Trading Tracker</h1>
            <p>Track your options positions with live stock prices from Yahoo Finance</p>
        </div>

        <div class="summary">
            <div class="summary-item">
                <div class="summary-label">Total Positions</div>
                <div class="summary-value" id="totalPositions">0</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Total Contracts</div>
                <div class="summary-value" id="totalContracts">0</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Total Profit</div>
                <div class="summary-value" id="totalProfit">$0</div>
            </div>
            <div class="summary-item">
                <div class="summary-label">Open Positions</div>
                <div class="summary-value" id="openPositions">0</div>
            </div>
        </div>

        <div class="controls">
            <button class="btn-success" onclick="addRow()">+ Add Position</button>
            <button class="btn-primary" id="refreshBtn" onclick="refreshPrices()">🔄 Refresh Prices</button>
            <button class="btn-secondary" onclick="exportData()">💾 Export Data</button>
            <button class="btn-secondary" onclick="importData()">📁 Import Data</button>
            <button class="btn-secondary" onclick="toggleDebug()">🔧 Debug Log</button>
        </div>

        <div class="progress-bar" id="progressBar">
            <div class="progress-fill" id="progressFill"></div>
        </div>

        <div class="debug-log" id="debugLog"></div>

        <div class="table-container">
            <table id="optionsTable">
                <thead>
                    <tr>
                        <th>Stock Symbol</th>
                        <th>Direction</th>
                        <th>Trade Date</th>
                        <th>Price at Purchase</th>
                        <th>Strike $</th>
                        <th onclick="sortTable('currentPrice')" style="cursor: pointer;">Current Stock Price ▲▼</th>
                        <th onclick="sortTable('difference')" style="cursor: pointer;">Stock Diff ▲▼</th>
                        <th onclick="sortTable('expiry')" style="cursor: pointer;">Expiry ▲▼</th>
                        <th onclick="sortTable('contracts')" style="cursor: pointer;"># Contracts ▲▼</th>
                        <th onclick="sortTable('soldPrice')" style="cursor: pointer;">Sold/Buy Price ▲▼</th>
                        <th onclick="sortTable('totalProfit')" style="cursor: pointer;">Total Profit ▲▼</th>
                        <th onclick="sortTable('gainPercent')" style="cursor: pointer;">% Gain to Strike ▲▼</th>
                        <th>Actions</th>
                    </tr>
                </thead>
                <tbody id="tableBody">
                </tbody>
            </table>
        </div>

        <div id="statusMessage"></div>
    </div>

    <script>
        let apiKey = ''; // Not needed for Yahoo Finance
        let positions = [];
        let isRefreshing = false;
        let sortColumn = null;
        let sortDirection = 'asc';

        // Initialize
        window.onload = function() {
            loadFromLocalStorage();
            if (positions.length === 0) {
                loadSampleData();
            }
            renderTable();
            updateSummary();
        };

        function sortTable(column) {
            // Toggle direction if clicking the same column
            if (sortColumn === column) {
                sortDirection = sortDirection === 'asc' ? 'desc' : 'asc';
            } else {
                sortColumn = column;
                sortDirection = 'asc';
            }

            // Sort the positions array
            positions.sort((a, b) => {
                let aVal, bVal;

                switch(column) {
                    case 'currentPrice':
                        aVal = a.currentPrice ?? -Infinity;
                        bVal = b.currentPrice ?? -Infinity;
                        break;
                    case 'difference':
                        aVal = calculateDifference(a) ?? -Infinity;
                        bVal = calculateDifference(b) ?? -Infinity;
                        break;
                    case 'expiry':
                        aVal = a.expiry ? new Date(a.expiry).getTime() : -Infinity;
                        bVal = b.expiry ? new Date(b.expiry).getTime() : -Infinity;
                        break;
                    case 'contracts':
                        aVal = a.contracts ?? 0;
                        bVal = b.contracts ?? 0;
                        break;
                    case 'soldPrice':
                        aVal = a.soldPrice ?? 0;
                        bVal = b.soldPrice ?? 0;
                        break;
                    case 'totalProfit':
                        aVal = calculateTotalProfit(a);
                        bVal = calculateTotalProfit(b);
                        break;
                    case 'gainPercent':
                        aVal = calculateGainPercent(a) ?? -Infinity;
                        bVal = calculateGainPercent(b) ?? -Infinity;
                        break;
                    default:
                        return 0;
                }

                if (sortDirection === 'asc') {
                    return aVal > bVal ? 1 : aVal < bVal ? -1 : 0;
                } else {
                    return aVal < bVal ? 1 : aVal > bVal ? -1 : 0;
                }
            });

            renderTable();
        }

        function showStatus(message, type) {
            const statusDiv = document.getElementById('statusMessage');
            statusDiv.className = `status status-${type}`;
            statusDiv.textContent = message;
            statusDiv.style.display = 'block';
            
            // Only auto-hide on success
            if (type === 'success') {
                setTimeout(() => {
                    statusDiv.style.display = 'none';
                }, 5000);
            }
            // For error/warning/info, keep visible so user can see what happened
        }

        function debugLog(message) {
            const debugDiv = document.getElementById('debugLog');
            const entry = document.createElement('div');
            entry.textContent = `[${new Date().toLocaleTimeString()}] ${message}`;
            debugDiv.appendChild(entry);
            debugDiv.scrollTop = debugDiv.scrollHeight;
            console.log(message);
        }

        function toggleDebug() {
            const debugDiv = document.getElementById('debugLog');
            debugDiv.classList.toggle('active');
        }

                function loadSampleData() {
            positions = [
  {"symbol": "CVS", "direction": "Put", "tradeDate": "2026-01-27", "purchasePrice": 71.75, "strike": 68.0, "currentPrice": null, "expiry": "2026-02-06", "contracts": 2, "soldPrice": 0.39},
  {"symbol": "MSFT", "direction": "Put", "tradeDate": "2026-01-30", "purchasePrice": 430.0, "strike": 420.0, "currentPrice": null, "expiry": "2026-02-13", "contracts": 1, "soldPrice": 4.05},
  {"symbol": "SEI", "direction": "Put", "tradeDate": "2026-01-22", "purchasePrice": 58.44, "strike": 42.5, "currentPrice": null, "expiry": "2026-02-20", "contracts": 1, "soldPrice": 1.1},
  {"symbol": "SEI", "direction": "Put", "tradeDate": "2026-01-22", "purchasePrice": 58.44, "strike": 37.5, "currentPrice": null, "expiry": "2026-02-20", "contracts": 1, "soldPrice": 0.45},
  {"symbol": "ISSC", "direction": "Put", "tradeDate": "2026-01-22", "purchasePrice": 21.17, "strike": 15.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 1, "soldPrice": 0.35},
  {"symbol": "ENVA", "direction": "Put", "tradeDate": "2026-02-02", "purchasePrice": 170.0, "strike": 155.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 2, "soldPrice": 2.5},
  {"symbol": "G", "direction": "Put", "tradeDate": "2026-01-27", "purchasePrice": 45.29, "strike": 40.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 2, "soldPrice": 1.3},
  {"symbol": "KMB", "direction": "Put", "tradeDate": "2026-01-26", "purchasePrice": 101.7, "strike": 98.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 1, "soldPrice": 1.33},
  {"symbol": "HMY", "direction": "Put", "tradeDate": "2026-01-26", "purchasePrice": 24.65, "strike": 23.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 4, "soldPrice": 0.9},
  {"symbol": "QCOM", "direction": "Put", "tradeDate": "2026-01-28", "purchasePrice": 153.05, "strike": 140.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 2, "soldPrice": 1.88},
  {"symbol": "CIB", "direction": "Put", "tradeDate": "2026-01-30", "purchasePrice": 80.81, "strike": 82.5, "currentPrice": null, "expiry": "2026-02-20", "contracts": 1, "soldPrice": 3.0},
  {"symbol": "ACN", "direction": "Put", "tradeDate": "2026-01-28", "purchasePrice": 268.9, "strike": 260.0, "currentPrice": null, "expiry": "2026-02-20", "contracts": 1, "soldPrice": 3.8},
  {"symbol": "FDS", "direction": "Put", "tradeDate": "2026-01-29", "purchasePrice": 269.62, "strike": 240.0, "currentPrice": null, "expiry": "2026-03-20", "contracts": 1, "soldPrice": 5.4},
  {"symbol": "OZK", "direction": "Put", "tradeDate": "2026-01-29", "purchasePrice": 47.04, "strike": 42.5, "currentPrice": null, "expiry": "2026-03-20", "contracts": 3, "soldPrice": 0.64},
  {"symbol": "EIX", "direction": "Put", "tradeDate": "2026-02-03", "purchasePrice": 61.76, "strike": 55.0, "currentPrice": null, "expiry": "2026-04-17", "contracts": 2, "soldPrice": 1.0},
  {"symbol": "ES", "direction": "Put", "tradeDate": "2026-01-30", "purchasePrice": 68.31, "strike": 65.0, "currentPrice": null, "expiry": "2026-04-17", "contracts": 2, "soldPrice": 1.65}
];
        }

        function addRow() {
            positions.push({
                symbol: '',
                direction: 'Put',
                tradeDate: new Date().toISOString().split('T')[0],
                purchasePrice: 0,
                strike: 0,
                currentPrice: null,
                expiry: '',
                contracts: 1,
                soldPrice: 0
            });
            renderTable();
            saveToLocalStorage();
        }

        function deleteRow(index) {
            if (confirm('Delete this position?')) {
                positions.splice(index, 1);
                renderTable();
                updateSummary();
                saveToLocalStorage();
            }
        }

        function renderTable() {
            const tbody = document.getElementById('tableBody');
            tbody.innerHTML = '';

            positions.forEach((pos, index) => {
                const row = tbody.insertRow();
                
                const cellSymbol = row.insertCell();
                cellSymbol.innerHTML = `<input type="text" value="${pos.symbol || ''}" onchange="updatePosition(${index}, 'symbol', this.value)" placeholder="AAPL">`;
                
                const cellDirection = row.insertCell();
                cellDirection.innerHTML = `
                    <select onchange="updatePosition(${index}, 'direction', this.value)">
                        <option value="Put" ${pos.direction === 'Put' ? 'selected' : ''}>Put</option>
                        <option value="Call" ${pos.direction === 'Call' ? 'selected' : ''}>Call</option>
                    </select>
                `;
                
                const cellTradeDate = row.insertCell();
                cellTradeDate.innerHTML = `<input type="date" value="${pos.tradeDate || ''}" onchange="updatePosition(${index}, 'tradeDate', this.value)">`;
                
                const cellPurchase = row.insertCell();
                cellPurchase.innerHTML = `<input type="number" step="0.01" value="${pos.purchasePrice || ''}" onchange="updatePosition(${index}, 'purchasePrice', parseFloat(this.value))">`;
                
                const cellStrike = row.insertCell();
                cellStrike.innerHTML = `<input type="number" step="0.01" value="${pos.strike || ''}" onchange="updatePosition(${index}, 'strike', parseFloat(this.value))">`;
                
                const cellCurrent = row.insertCell();
                const currentPriceDisplay = pos.currentPrice !== null ? `$${pos.currentPrice.toFixed(2)}` : '-';
                cellCurrent.innerHTML = `${currentPriceDisplay}`;
                cellCurrent.style.textAlign = 'center';
                
                const cellDiff = row.insertCell();
                const diff = calculateDifference(pos);
                const diffClass = diff < 0 ? 'negative' : diff > 0 ? 'positive' : '';
                const diffDisplay = diff !== null ? `${diff < 0 ? '' : '+'}${diff.toFixed(2)}` : '-';
                cellDiff.innerHTML = `<span class="${diffClass}" style="font-size: 13px;">${diffDisplay}</span>`;
                cellDiff.style.textAlign = 'center';
                
                const cellExpiry = row.insertCell();
                cellExpiry.innerHTML = `<input type="date" value="${pos.expiry || ''}" onchange="updatePosition(${index}, 'expiry', this.value)">`;
                
                const cellContracts = row.insertCell();
                cellContracts.innerHTML = `<input type="number" value="${pos.contracts || ''}" onchange="updatePosition(${index}, 'contracts', parseInt(this.value))">`;
                
                const cellSold = row.insertCell();
                cellSold.innerHTML = `<input type="number" step="0.01" value="${pos.soldPrice || ''}" onchange="updatePosition(${index}, 'soldPrice', parseFloat(this.value))">`;
                
                const cellTotalProfit = row.insertCell();
                const totalProfit = calculateTotalProfit(pos);
                const profitClass = totalProfit < 0 ? 'negative' : totalProfit > 0 ? 'positive' : '';
                cellTotalProfit.innerHTML = `<span class="${profitClass}">$${totalProfit.toFixed(0)}</span>`;
                cellTotalProfit.style.textAlign = 'center';
                
                const cellGain = row.insertCell();
                const gainPercent = calculateGainPercent(pos);
                const gainClass = gainPercent < 0 ? 'negative' : gainPercent > 0 ? 'positive' : '';
                const gainDisplay = gainPercent !== null ? `${(gainPercent * 100).toFixed(2)}%` : '-';
                cellGain.innerHTML = `<span class="${gainClass}">${gainDisplay}</span>`;
                cellGain.style.textAlign = 'center';
                
                const cellActions = row.insertCell();
                cellActions.innerHTML = `<button class="btn-delete" onclick="deleteRow(${index})">Delete</button>`;
            });

            updateSummary();
        }

        function calculateDifference(pos) {
            if (pos.currentPrice !== null && pos.strike) {
                return pos.currentPrice - pos.strike;
            }
            return null;
        }

        function calculateTotalProfit(pos) {
            if (pos.soldPrice && pos.contracts) {
                return pos.soldPrice * pos.contracts * 100;
            }
            return 0;
        }

        function calculateGainPercent(pos) {
            if (pos.purchasePrice && pos.strike) {
                return (pos.purchasePrice - pos.strike) / pos.strike;
            }
            return null;
        }

        function updatePosition(index, field, value) {
            positions[index][field] = value;
            renderTable();
            saveToLocalStorage();
        }

        async function refreshPrices() {
            if (isRefreshing) {
                showStatus('Already refreshing prices...', 'warning');
                return;
            }

            const symbols = [...new Set(positions.filter(p => p.symbol).map(p => p.symbol.toUpperCase()))];
            
            if (symbols.length === 0) {
                showStatus('No stock symbols to fetch', 'error');
                return;
            }

            isRefreshing = true;
            document.getElementById('refreshBtn').disabled = true;
            document.getElementById('progressBar').classList.add('active');
            document.getElementById('debugLog').classList.add('active');
            document.getElementById('debugLog').innerHTML = '';
            
            showStatus(`Fetching prices for ${symbols.length} stocks from Yahoo Finance... This should take ~${Math.ceil(symbols.length * 2)} seconds`, 'info');
            debugLog(`Starting price fetch for ${symbols.length} symbols: ${symbols.join(', ')}`);

            let successCount = 0;
            let failCount = 0;

            for (let i = 0; i < symbols.length; i++) {
                const symbol = symbols[i];
                const progress = ((i + 1) / symbols.length) * 100;
                document.getElementById('progressFill').style.width = `${progress}%`;
                
                debugLog(`[${i+1}/${symbols.length}] Fetching ${symbol}...`);
                
                try {
                    // Yahoo Finance API endpoint
                    const yahooUrl = `https://query1.finance.yahoo.com/v8/finance/chart/${symbol}`;
                    debugLog(`Fetching from Yahoo Finance: ${yahooUrl}`);
                    
                    let response;
                    let data;
                    
                    try {
                        // Try direct fetch first
                        response = await fetch(yahooUrl);
                        data = await response.json();
                        debugLog(`Direct fetch succeeded for ${symbol}`);
                    } catch (directError) {
                        // If direct fails, try CORS proxy
                        debugLog(`Direct fetch failed for ${symbol}, trying CORS proxy...`);
                        const proxyUrl = `https://corsproxy.io/?${encodeURIComponent(yahooUrl)}`;
                        response = await fetch(proxyUrl);
                        data = await response.json();
                        debugLog(`CORS proxy fetch succeeded for ${symbol}`);
                    }

                    debugLog(`Response for ${symbol}: ${JSON.stringify(data).substring(0, 300)}...`);

                    // Extract price from Yahoo Finance response
                    if (data.chart && data.chart.result && data.chart.result[0]) {
                        const result = data.chart.result[0];
                        const price = result.meta.regularMarketPrice;
                        
                        if (price) {
                            debugLog(`✓ Got price for ${symbol}: $${price}`);
                            
                            positions.forEach(pos => {
                                if (pos.symbol.toUpperCase() === symbol) {
                                    pos.currentPrice = price;
                                }
                            });
                            
                            successCount++;
                            renderTable();
                        } else {
                            debugLog(`✗ No price data in response for ${symbol}`);
                            failCount++;
                        }
                    } else {
                        debugLog(`✗ Invalid response structure for ${symbol}. Response: ${JSON.stringify(data)}`);
                        failCount++;
                    }

                    // Small delay to be respectful (not required by Yahoo, but good practice)
                    if (i < symbols.length - 1) {
                        debugLog(`Waiting 1 second before next request...`);
                        await new Promise(resolve => setTimeout(resolve, 1000));
                    }
                } catch (error) {
                    debugLog(`✗ Error fetching ${symbol}: ${error.message}`);
                    console.error(`Error fetching ${symbol}:`, error);
                    failCount++;
                }
            }

            isRefreshing = false;
            document.getElementById('refreshBtn').disabled = false;
            document.getElementById('progressBar').classList.remove('active');
            document.getElementById('progressFill').style.width = '0%';
            
            saveToLocalStorage();
            
            if (successCount === symbols.length) {
                showStatus(`✓ Successfully updated all ${successCount} stock prices!`, 'success');
                debugLog(`✓ Refresh complete: ${successCount} successful, ${failCount} failed`);
            } else if (successCount > 0) {
                showStatus(`Updated ${successCount} of ${symbols.length} prices. ${failCount} failed - check debug log.`, 'warning');
                debugLog(`⚠ Refresh complete: ${successCount} successful, ${failCount} failed`);
            } else {
                showStatus(`Failed to fetch any prices. Check debug log for details.`, 'error');
                debugLog(`✗ Refresh failed: 0 successful, ${failCount} failed`);
            }
        }

        function updateSummary() {
            const total = positions.length;
            const totalContracts = positions.reduce((sum, pos) => sum + (pos.contracts || 0), 0);
            const totalProfit = positions.reduce((sum, pos) => sum + calculateTotalProfit(pos), 0);
            const open = positions.filter(pos => {
                if (!pos.expiry) return false;
                return new Date(pos.expiry) >= new Date();
            }).length;

            document.getElementById('totalPositions').textContent = total;
            document.getElementById('totalContracts').textContent = totalContracts;
            document.getElementById('totalProfit').textContent = `$${totalProfit.toFixed(0)}`;
            document.getElementById('openPositions').textContent = open;

            const profitElement = document.getElementById('totalProfit');
            profitElement.className = 'summary-value ' + (totalProfit >= 0 ? 'positive' : 'negative');
        }

        function saveToLocalStorage() {
            localStorage.setItem('optionsPositions', JSON.stringify(positions));
        }

        function loadFromLocalStorage() {
            const saved = localStorage.getItem('optionsPositions');
            if (saved) {
                positions = JSON.parse(saved);
            }
        }

        function exportData() {
            const dataStr = JSON.stringify(positions, null, 2);
            const dataUri = 'data:application/json;charset=utf-8,' + encodeURIComponent(dataStr);
            const exportFileDefaultName = `options-tracker-${new Date().toISOString().split('T')[0]}.json`;
            
            const linkElement = document.createElement('a');
            linkElement.setAttribute('href', dataUri);
            linkElement.setAttribute('download', exportFileDefaultName);
            linkElement.click();
            
            showStatus('Data exported successfully!', 'success');
        }

        function importData() {
            const input = document.createElement('input');
            input.type = 'file';
            input.accept = '.json';
            input.onchange = function(event) {
                const file = event.target.files[0];
                const reader = new FileReader();
                reader.onload = function(e) {
                    try {
                        positions = JSON.parse(e.target.result);
                        renderTable();
                        updateSummary();
                        saveToLocalStorage();
                        showStatus('Data imported successfully!', 'success');
                    } catch (error) {
                        showStatus('Error importing data. Please check the file format.', 'error');
                    }
                };
                reader.readAsText(file);
            };
            input.click();
        }
    </script>
</body>
</html>
