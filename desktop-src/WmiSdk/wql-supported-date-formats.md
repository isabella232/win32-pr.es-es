---
description: Describe los formatos de fecha admitidos para su uso en la cláusula WQL WHERE.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported formatos de fecha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910270"
---
# <a name="wql-supported-date-formats"></a>WQL-Supported formatos de fecha

Además del formato **DateTime** de WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula **Where** de WQL.

El formato de hora mostrado es diferente para las distintas configuraciones regionales. Los scripts que se conectan a los equipos remotos deben especificar la hora con el formato adecuado para la configuración regional del equipo de destino.

Por ejemplo, el formato de fecha y hora Estados Unidos es MM-DD-YYYY. Si un script de un equipo de EE. UU. se conecta a un equipo de destino en una configuración regional en la que el formato es DD-MM-AAAA, las consultas se procesan en el equipo de destino como DD-MM-AAAA. Para evitar distintos resultados entre configuraciones regionales, use el formato de [**fecha y hora**](datetime.md) . Para obtener más información, vea [formato de fecha y hora](date-and-time-format.md).



<table>
<thead>
<tr class="header">
<th>Formato</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mon [th] DD [,] [AA] AA</td>
<td>Mes (deletreado o abreviado en tres letras), día, coma opcional y dos o cuatro dígitos de año.<br/> <dl> 21 de enero de 1932<br />
21 de enero de 32<br />
21 1932 de enero<br />
21 32 de enero<br />
</dl></td>
</tr>
<tr class="even">
<td>Mon [th] [,] AAAA</td>
<td>Mes (deletreado o abreviado en tres letras), una coma opcional y un año de cuatro dígitos.<br/> <dl> 1932 de enero<br />
1932 de enero<br />
</dl></td>
</tr>
<tr class="odd">
<td>Mon [th] [yy] yy DD</td>
<td>Mes (deletreado o abreviado en tres letras), dos o cuatro dígitos de año y día.<br/> <dl> 1932 21 de enero<br />
32 21 de enero<br />
</dl></td>
</tr>
<tr class="even">
<td>DD mes [th] [,] [] [AA] AA</td>
<td>Día del mes, mes (deletreado o abreviado en tres letras), coma opcional, espacio opcional y dos o cuatro dígitos de año.<br/> <dl> 21 de enero de 1932<br />
21 Jan32<br />
</dl></td>
</tr>
<tr class="odd">
<td>DD [AA] AA Mon [th]</td>
<td>Día del mes, dos o cuatro dígitos año y mes (deletreado o abreviado en tres letras).<br/> <dl> 21 1932 de enero<br />
</dl></td>
</tr>
<tr class="even">
<td>[yy] yy mes [th] DD</td>
<td>Año de dos o cuatro dígitos, mes (deletreado o abreviado en tres letras) y día.<br/> <dl> 21 de enero de 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>yyyy Mon [th]</td>
<td>Año y mes de dos o cuatro dígitos (deletreado o abreviado en tres letras).<br/> <dl> 1932 de enero<br />
</dl></td>
</tr>
<tr class="even">
<td>AAAA DD mes [th]</td>
<td>Año, día y mes de dos o cuatro dígitos (deletreado o abreviado en tres letras).<br/> <dl> 1932 21 de enero<br />
</dl></td>
</tr>
<tr class="odd">
<td>F M {/-.} DD {/-.} [yy] AA</td>
<td>Mes, día y dos o cuatro dígitos de año. Tenga en cuenta que los separadores deben ser iguales.<br/></td>
</tr>
<tr class="even">
<td>DD {/-.} F M {/-.} [yy] AA</td>
<td>Día del mes, mes y año de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser iguales.<br/></td>
</tr>
<tr class="odd">
<td>F M {/-.} [yy] yy {/-.} DD</td>
<td>Mes, dos o cuatro dígitos de año y día. Tenga en cuenta que los separadores deben ser iguales.<br/></td>
</tr>
<tr class="even">
<td>DD {/-.} [yy] yy {/-.} F F</td>
<td>Día del mes, dos o cuatro dígitos de año y mes. Tenga en cuenta que los separadores deben ser iguales.<br/></td>
</tr>
<tr class="odd">
<td>[yy] yy {/-.} DD {/-.} F F</td>
<td>Año, día y mes de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser iguales.<br/></td>
</tr>
<tr class="even">
<td>[yy] yy {/-.} F M {/-.} DD</td>
<td>Año, mes y día de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser iguales.<br/></td>
</tr>
<tr class="odd">
<td>[yy] AAMMDD</td>
<td>Dos o cuatro dígitos de año, mes y día, sin espacios.<br/></td>
</tr>
<tr class="even">
<td>aaaa [MM [DD]]</td>
<td>Año de dos o cuatro dígitos, un mes opcional y un día opcional, sin espacios.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




