---
description: Describe los formatos de fecha admitidos para su uso en la cláusula WHERE de WQL.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported formatos de fecha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0451778d82905b5ec74d4e6feecb62a63ab630d83a9a5db81f2a10a0488b7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118106979"
---
# <a name="wql-supported-date-formats"></a>WQL-Supported formatos de fecha

Además del formato **DATETIME de** WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula **WHERE** de WQL.

El formato de hora mostrado es diferente para distintas configuraciones regionales. Los scripts que se conectan a equipos remotos deben especificar la hora en el formato adecuado para la configuración regional del equipo de destino.

Por ejemplo, el Estados Unidos de fecha y hora es MM-DD-YYYY. Si un script de un equipo de Estados Unidos se conecta a un equipo de destino en una configuración regional donde el formato es DD-MM-YYYY, las consultas se procesan en el equipo de destino como DD-MM-YYYY. Para evitar resultados diferentes entre configuraciones regionales, use el [**formato DATETIME.**](datetime.md) Para obtener más información, vea [Formato de fecha y hora.](date-and-time-format.md)



<table>
<thead>
<tr class="header">
<th>Formato</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mon[th] dd[,] [yy]yy</td>
<td>Mes (escrito o abreviado en tres letras), día, coma opcional y año de dos o cuatro dígitos.<br/> <dl> 21 de enero de 1932<br />
21 de enero de 32<br />
21 de enero de 1932<br />
21 de enero de 32<br />
</dl></td>
</tr>
<tr class="even">
<td>Mon[th][,] yyyy</td>
<td>Mes (escrito o abreviado en tres letras), coma opcional y año de cuatro dígitos.<br/> <dl> Enero de 1932<br />
Enero de 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>Mon[th] [yy]yy dd</td>
<td>Mes (escrito o abreviado en tres letras), año de dos o cuatro dígitos y día.<br/> <dl> Enero de 1932, 21<br />
32 de enero de 21<br />
</dl></td>
</tr>
<tr class="even">
<td>dd Mon[th][,][ ][yy]yy</td>
<td>Día del mes, mes (escrito o abreviado en tres letras), coma opcional, espacio opcional y año de dos o cuatro dígitos.<br/> <dl> 21 de enero de 1932<br />
21 ene32<br />
</dl></td>
</tr>
<tr class="odd">
<td>dd [yy]yy Mon[th]</td>
<td>Día del mes, año de dos o cuatro dígitos y mes (escrito o abreviado en tres letras).<br/> <dl> 21 de enero de 1932<br />
</dl></td>
</tr>
<tr class="even">
<td>[yy]yy Mon[th] dd</td>
<td>Año de dos o cuatro dígitos, mes (escrito o abreviado en tres letras) y día.<br/> <dl> 21 de enero de 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>yyyy Mon[th]</td>
<td>Año y mes de dos o cuatro dígitos (escritos o abreviados en tres letras).<br/> <dl> Enero de 1932<br />
</dl></td>
</tr>
<tr class="even">
<td>yyyy dd Mon[th]</td>
<td>Año, día y mes de dos o cuatro dígitos (escritos o abreviados en tres letras).<br/> <dl> 21 de enero de 1932<br />
</dl></td>
</tr>
<tr class="odd">
<td>[M] M{/-.} dd{/-.} [yy]yy</td>
<td>Mes, día y año de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser los mismos.<br/></td>
</tr>
<tr class="even">
<td>dd{/-.} [M] M{/-.} [yy]yy</td>
<td>Día del mes, mes y año de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser los mismos.<br/></td>
</tr>
<tr class="odd">
<td>[M] M{/-.} [yy]yy{/-.} Dd</td>
<td>Mes, año de dos o cuatro dígitos y día. Tenga en cuenta que los separadores deben ser los mismos.<br/></td>
</tr>
<tr class="even">
<td>dd{/-.} [yy]yy{/-.} [M] M</td>
<td>Día del mes, año de dos o cuatro dígitos y mes. Tenga en cuenta que los separadores deben ser los mismos.<br/></td>
</tr>
<tr class="odd">
<td>[yy]yy{/-.} dd{/-.} [M] M</td>
<td>Año, día y mes de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser los mismos.<br/></td>
</tr>
<tr class="even">
<td>[yy]yy{/-.} [M] M{/-.} Dd</td>
<td>Año, mes y día de dos o cuatro dígitos. Tenga en cuenta que los separadores deben ser los mismos.<br/></td>
</tr>
<tr class="odd">
<td>[yy]yyMMdd</td>
<td>Año, mes y día de dos o cuatro dígitos, sin espacios.<br/></td>
</tr>
<tr class="even">
<td>yyyy[MM[dd]]</td>
<td>Año de dos o cuatro dígitos, mes opcional y día opcional, sin espacios.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cláusula WHERE](where-clause.md)
</dt> </dl>

 

 




