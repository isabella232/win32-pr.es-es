---
description: Especifica el número máximo de marcos de referencia a largo plazo (LTR) controlados por la aplicación.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Propiedad CODECAPI_AVEncVideoLTRBufferControl (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539627"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>\_Propiedad AVEncVideoLTRBufferControl de CODECAPI

Especifica el número máximo de marcos de referencia a largo plazo (LTR) controlados por la aplicación.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>Valor de propiedad

El valor de este control incluye dos campos, donde cada campo tiene 16 bits.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>Los primeros bits de campo</strong></dt> <dt>[0.. 15]</dt> </dl></td>
<td>El número de Marcos LTR controlados por la aplicación.<br/> <strong>Codificadores H. 264/AVC:</strong><br/> Suponiendo que el valor es N y N es un valor distinto de cero, en cada fotograma de IDR el codificador debe marcar automáticamente los fotogramas que siguen al fotograma IDR (incluido el fotograma de IDR) como marcos LTR, siempre y cuando se apliquen las 3 siguientes:
<ul>
<li>El marco no se ha establecido para que se marque como marco de referencia a largo plazo.</li>
<li>El marco es un marco de nivel base. Por ejemplo, el elemento de sintaxis <strong>temporal_id</strong> igual a 0.</li>
<li>El número de fotogramas marcados actualmente como LTR es menor que N.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Los bits del segundo campo</strong></dt> <dt>[16.. 31]</dt> </dl></td>
<td>El modo de confianza de control LTR.<br/> <strong>Codificadores H. 264/AVC:</strong><br/> 1 (confiar hasta) significa que el codificador puede usar un marco LTR a menos que la aplicación lo invalide explícitamente a través del control <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br/> Otros valores no son válidos y se reservan para uso futuro.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Se trata de una API estática.

El valor predeterminado debe ser 0

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                   |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




