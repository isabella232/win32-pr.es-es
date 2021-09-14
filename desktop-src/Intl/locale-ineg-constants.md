---
description: En este tema se definen las constantes \_ INEG de LOCALE \* usadas por NLS.
ms.assetid: 3a1e4a63-31bd-4ff9-a3ca-af357389e179
title: LOCALE_INEG* Constantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb5c40b2fc53e93653753eeb61048251a7fe55c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274500"
---
# <a name="locale_ineg-constants"></a>Constantes \_ INEG de LOCALE \*

En este tema se definen las constantes \_ INEG de LOCALE \* usadas por NLS.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LOCALE_INEGCURR</td>
<td>Modo de moneda negativo. 
<table>
<thead>
<tr class="header">
<th>Modo</th>
<th>Formato de moneda negativa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Paréntesis de apertura, símbolo monetario, número, paréntesis derecho; por ejemplo, (1,1 USD)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Signo negativo, símbolo monetario, número; por ejemplo, -$1,1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Símbolo monetario, signo negativo, número; por ejemplo, $-1.1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Símbolo monetario, número, signo negativo; por ejemplo, $1,1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Paréntesis izquierdos, número, símbolo monetario, paréntesis derecho; por ejemplo, (1,1 $)</td>
</tr>
<tr class="even">
<td>5</td>
<td>Signo negativo, número, símbolo monetario; por ejemplo, -1,1$</td>
</tr>
<tr class="odd">
<td>6</td>
<td>Number, negative sign, monetary symbol; por ejemplo, 1,1-$</td>
</tr>
<tr class="even">
<td>7</td>
<td>Number, monetary symbol, negative sign; por ejemplo, 1,1$-</td>
</tr>
<tr class="odd">
<td>8</td>
<td>Signo negativo, número, espacio, símbolo monetario (como #5, pero con un espacio antes del símbolo monetario); por ejemplo, -1,1 $</td>
</tr>
<tr class="even">
<td>9</td>
<td>Signo negativo, símbolo monetario, espacio, número (como #1, pero con un espacio después del símbolo monetario); por ejemplo, -$ 1,1</td>
</tr>
<tr class="odd">
<td>10</td>
<td>Número, espacio, símbolo monetario, signo negativo (como #7, pero con un espacio delante del símbolo monetario); por ejemplo, 1,1 $-</td>
</tr>
<tr class="even">
<td>11</td>
<td>Símbolo monetario, espacio, número, signo negativo (como #3, pero con un espacio después del símbolo monetario); por ejemplo, 1,1 $</td>
</tr>
<tr class="odd">
<td>12</td>
<td>Símbolo monetario, espacio, signo negativo, número (como #2, pero con un espacio después del símbolo monetario); por ejemplo, $ -1,1</td>
</tr>
<tr class="even">
<td>13</td>
<td>Número, signo negativo, espacio, símbolo monetario (como #6, pero con un espacio delante del símbolo monetario); por ejemplo, 1,1- $</td>
</tr>
<tr class="odd">
<td>14</td>
<td>Paréntesis de apertura, símbolo monetario, espacio, número, paréntesis derecho (como #0, pero con un espacio después del símbolo monetario); por ejemplo, ($ 1,1)</td>
</tr>
<tr class="even">
<td>15</td>
<td>Paréntesis de apertura, número, espacio, símbolo monetario, paréntesis derecho (como #4, pero con un espacio antes del símbolo monetario); por ejemplo, (1,1 $)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>LOCALE_INEGNUMBER</td>
<td>Modo de número negativo, es decir, el formato de un número negativo. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Formato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Paréntesis izquierdo, número, paréntesis derecho; por ejemplo, (1.1)</td>
</tr>
<tr class="even">
<td>1</td>
<td>Signo negativo, número; por ejemplo, -1.1</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Signo negativo, espacio, número; por ejemplo, - 1.1</td>
</tr>
<tr class="even">
<td>3</td>
<td>Número, signo negativo; por ejemplo, 1.1-</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Número, espacio, signo negativo; por ejemplo, 1.1 :</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSEPBYSPACE</td>
<td>Separación del signo negativo en un valor monetario. Este valor es 1 si el símbolo monetario está separado por un espacio de la cantidad negativa, o 0 si no lo está.</td>
</tr>
<tr class="even">
<td>LOCALE_INEGSIGNPOSN</td>
<td>Índice de formato para los valores de moneda de inicio de sesión negativos. 
<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Los paréntesis rodean la cantidad y el símbolo monetario.</td>
</tr>
<tr class="even">
<td>1</td>
<td>El signo precede al número.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>El signo sigue al número.</td>
</tr>
<tr class="even">
<td>3</td>
<td>El signo precede al símbolo monetario.</td>
</tr>
<tr class="odd">
<td>4</td>
<td>El signo sigue al símbolo monetario.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>LOCALE_INEGSYMPRECEDES</td>
<td>Posición del símbolo monetario en un valor monetario negativo. Este valor es 1 si el símbolo monetario precede a la cantidad negativa, o 0 si el símbolo sigue a la cantidad.</td>
</tr>
</tbody>
</table>



 

 

 



