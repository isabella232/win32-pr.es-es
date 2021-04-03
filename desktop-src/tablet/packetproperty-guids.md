---
description: En la tabla siguiente se enumeran los GUID de propiedades de paquete utilizados por la estructura de propiedades de paquetes \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID de PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913546"
---
# <a name="packetproperty-guids"></a>GUID de PacketProperty

En la tabla siguiente se enumeran los GUID de propiedades de paquete utilizados por la estructura de [**\_ propiedades de paquetes**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GUID_ALTITUDE_ORIENTATION<br/></td>
<td>Ángulo entre el eje del lápiz y la superficie de la tableta. El valor es 0 cuando el lápiz es paralelo a la superficie y 90 cuando el lápiz es perpendicular a la superficie. Los valores son negativos cuando se invierte el lápiz.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Rotación en el sentido de las agujas del reloj del cursor alrededor del eje z a través de un intervalo circular completo.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>GUID que se usa para recuperar el número de cuadro de una alternativa de reconocimiento de tinta cuando el reconocedor está funcionando en modo de cuadro.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Presión sobre un botón sensible a la presión.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>El GUID para el objeto PacketProperty que representa la presión de la punta del lápiz perpendicular a la superficie de la tableta. Cuanto mayor sea la presión de la punta del lápiz, más tinta se dibujará.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Contiene uno o varios de los siguientes valores de marca:<br/>
<ul>
<li>El cursor toca la superficie de dibujo (valor = 1).</li>
<li>El cursor se invierte. Por ejemplo, el extremo del borrador del lápiz apunta hacia la superficie (valor = 2).</li>
<li>No se usa (valor = 4).</li>
<li>Se presiona el botón de barril (valor = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>Identificador de contacto del dispositivo para un paquete.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifica el paquete. Este es el mismo valor que se usa para recuperar el paquete de la cola de paquetes.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>El GUID para el objeto PacketProperty que representa la presión de la punta del lápiz a lo largo del plano de la superficie de Tablet PC.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Hora a la que se generó el paquete.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Rotación en el sentido de las agujas del reloj del cursor alrededor de su propio eje.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Coordenada x del espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>En el caso de un cursor de lápiz, la orientación de la inclinación x es el ángulo entre el plano y, z y el plano del eje y y el lápiz. El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está a la derecha de la perpendicular.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Coordenada y del espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Para un cursor de lápiz, la orientación de inclinación y es el ángulo entre el plano x, z y el lápiz y el plano del eje x. El valor es 0 cuando el lápiz es perpendicular a la superficie de dibujo y es positivo cuando el lápiz está hacia arriba o fuera del usuario.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>La coordenada z o la distancia de la punta del lápiz desde la superficie de la tableta. El tipo de enumeración <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> determina la unidad de medida para esta propiedad. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> El campo TangentPressure representa la presión a lo largo del plano de la superficie de la tableta. el campo NormalPressure representa la presión perpendicular al plano de la superficie de Tablet PC.

 

 

 




