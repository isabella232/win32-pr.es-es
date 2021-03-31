---
description: Especifica que el marco actual está codificado con uno o varios marcos LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Propiedad CODECAPI_AVEncVideoUseLTRFrame (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808167"
---
# <a name="codecapi_avencvideouseltrframe-property"></a>\_Propiedad AVEncVideoUseLTRFrame de CODECAPI

Especifica que el marco actual está codificado con uno o varios marcos LTR.

## <a name="data-type"></a>Tipo de datos

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVEncVideoUseLTRFrame**

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
<td>Indica qué Marcos LTR están permitidos para codificar el marco actual. <br/> <strong>Codificadores H. 264/AVC:</strong><br/> Se trata de un mapa de bits que indica qué marcos de LTR se pueden usar como referencia para este marco. El bit menos significativo corresponde al índice 0 LTR, el segundo bit menos significativo corresponde al índice 1, etc.<br/> Este valor no debe ser 0.<br/> El índice más alto especificado por este valor no debe ser mayor que el número máximo de Marcos LTR especificado en la propiedad <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> menos uno.<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Los bits del segundo campo</strong></dt> <dt>[16.. 31]</dt> </dl></td>
<td>Marca que indica si se requieren limitaciones adicionales para codificar fotogramas posteriores. <br/> <strong>Codificadores H. 264/AVC:</strong><br/> 1 está en el único valor válido para este campo. Todos los demás valores no son válidos y se reservan para uso futuro.<br/> Cuando la marca es 1, el codificador debe codificar los fotogramas posteriores en el orden de codificación de acuerdo con las restricciones siguientes:<br/>
<ul>
<li>No debe utilizar fotogramas de referencia a corto plazo en el orden de codificación anterior al marco actual o la codificación futura en el orden de codificación.</li>
<li>No debe usar marcos LTR no descritos por el control CODECAPI_AVEncVideoUseLTRFrame más reciente.</li>
<li>Puede usar marcos LTR actualizados después del fotograma actual.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

**Codificadores H. 264/AVC:**

No se debe llamar a esta propiedad si se ha emitido una llamada pendiente para usar un marco LTR mediante la \_ propiedad CODECAPI AVEncVideoUseLTRFrame y el codificador aún no ha generado un fotograma que ha usado LTR. En otras palabras, el codificador no debe poner en cola \_ las solicitudes de CODECAPI AVEncVideoUseLTRFrame.

Si \_ se envía una solicitud AVEncVideoUseLTRFrame de CODECAPI mientras otra \_ solicitud AVENCVIDEOUSELTRFRAME de CODECAPI está pendiente, se debe quitar la solicitud anterior.

Llamar a CODECAPI \_ AVEncVideoUseLTRFrame en un marco de capa no base es válido y se aplicará al fotograma de capa no base, sin retrasar a un fotograma Base de la capa.

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

 

 




