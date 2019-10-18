# spa_test
ashrap.github.io <a href="http://ashrap.github.io"><b>DEMO</b></a>
<hr>
++ <b>SPA</b></br>
++ <b>VueJS</b></br>
++ <b>VueRouter</b></br>
++ <b>Vuex</b></br>
++ <b>Webpack</b></br>
++ <b>WebSocket</b>


#<b>1 На первой странице компонент:</b></br></br>
1.1 По <b>REST</b> забирает состояние по определенному символу с биржи binance ( limit=500 ) и отрисовывает состояние в формате:</br></br>
Amount--Price--Total || Amount--Price--Total</br></br>
Где левые три колонки относятся к ордерам типа Bid, правые к ордерам типа Ask. 
Price и Amount (Quantity) получаются из binance. Total рассчитывается на клиенте как Price * Amount.
</br>
</br>
1.2 Подключается на обновления данных по <b>WebSocket</b> для этого символа (по умолчанию берется по BNBBTC)
<hr>
<b>2 На второй странице компонент, содержащий DropDown с перечнем символов</b></br></br>
2.1 DropDown при изменении выбранного элемента отправляет в шину данных(<b>Vuex</b>) событие об изменении активного символа</br></br>
2.2 Cписочный элемент читает шину данных и отображает информацию о каждом diff-изменении в новой строке.
<hr>
<b>3 Верстка резиновая и адаптивная для мобилки и десктопа.</b></br></br> 
В мобильной версии отображаются только колонки с Price и Amount. Где левые две колонки относятся к ордерам типа Bid, правые к ордерам типа Ask. 
<hr>
