<template>
            <div class="app-admin-section">
            <div class="app-admin-col-1">
            <Leftbar/>
            </div>
            <div class="app-admin-col-2">
            <div class="admin-top-bar">
        <div class="admin-top-bar-left">
          <div class="settings-icon"></div>
        </div>
        <div class="admin-top-bar-right">
          <div class="admin-topbar-date">{{new Date().utc | humanize}}</div>
        </div>
      </div>
            <div class="content-header">Hii there! <span>{{ user.person.firstName }}</span></div>
              <div class="content-sub2"> Here are the latest report on account</div>
              <div class="summary-flex">
                                   <div class="content-slide-box">
                      <div class="content-info-card">
                        <div class="div-block-2">
                          <div class="slide-card-header">Total Savings</div>
                          <div class="slide-card-value">N0</div>
                        </div>
                        <div class="slide-card-icon green"></div>
                      </div>
                    </div>
                     <div class="content-slide-box">
                      <div class="content-info-card">
                        <div class="div-block-2">
                          <div class="slide-card-header">Loan Requests</div>
                          <div class="slide-card-value">N0</div>
                        </div>
                        <div class="slide-card-icon green"></div>
                      </div>
                    </div>
                      <div class="content-slide-box">
                      <div class="content-info-card">
                        <div class="div-block-2">
                          <div class="slide-card-header">Total Transactions</div>
                          <div class="slide-card-value">N0</div>
                        </div>
                        <div class="slide-card-icon green"></div>
                      </div>
                    </div>
              </div>
              <div class="basic-table-card">
                <div class="table-header">
                  <div class="content-header-2">Recent Transactions</div>
                  <div class="table-view-all">View all</div>
                </div>
                
                <table class="app-table">
										<thead>
											<tr class="app-table-row">
                      <th class="app-table-header">Ref.ID</th>
											<th class="app-table-header">Trans.Details</th>
                      <th class="app-table-header">Trans.Type</th>
											<th class="app-table-header">Trans.Status</th>
                      <th class="app-table-header">Date</th>
										</tr>
										</thead>

										<tbody>
                  <tr class="app-table-row">
                      <td  class="app-table-data">CHV-783487242</td>
                     <td class="app-table-data">Trf:/N60,000/EMP-ID-4838/</td>
                     <td class="app-table-data">Transfer</td>
                     <td class="app-table-data">Success</td>
                     <td class="app-table-data">12/03/21</td>
                   </tr>
                     <tr class="app-table-row">
                      <td  class="app-table-data">CHV-783487242</td>
                     <td class="app-table-data">Withdrawal:/N30,000/EMP-ID-4838/</td>
                     <td class="app-table-data">Withdrawal</td>
                     <td class="app-table-data">Success</td>
                     <td class="app-table-data">12/03/21</td>
                   </tr>
                     <tr class="app-table-row">
                      <td  class="app-table-data">CHV-783487242</td>
                     <td class="app-table-data">Trf:/N20,000/EMP-ID-4838/</td>
                     <td class="app-table-data">Transfer</td>
                     <td class="app-table-data">Success</td>
                     <td class="app-table-data">12/03/21</td>
                   </tr>
                    <tr class="app-table-row">
                      <td  class="app-table-data">CHV-783487242</td>
                     <td class="app-table-data">Withdrawal:/N90,000/EMP-ID-4838/</td>
                     <td class="app-table-data">Withdrawal</td>
                     <td class="app-table-data">Success</td>
                     <td class="app-table-data">12/03/21</td>
                   </tr>
										</tbody>
										
										
										</table>
              </div>
            </div>
            <div class="app-admin-col-3">
              <Rightbar />
            </div>
          </div>
</template>

<script src="./dashboard.js"></script>

<style src=".././global.css"></style>