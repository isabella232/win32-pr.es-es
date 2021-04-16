---
description: Especifica los valores de calidad visual óptimos que se usarán para el codificador de perfil avanzado de Windows Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: Propiedad MFPKEY_COMPRESSIONOPTIMIZATIONTYPE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3000caa10aa7db7d201cd11fd9a189fd6ac33591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696954"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>\_Propiedad COMPRESSIONOPTIMIZATIONTYPE de MFPKEY

Especifica los valores de calidad visual óptimos que se usarán para el codificador de perfil avanzado de Windows Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad proporciona una manera rápida de configurar una serie de opciones de codificación de vídeo. Se puede establecer en uno de los valores siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>El códec no forzará la optimización y usará las características especificadas por otras propiedades. En muchos casos, el códec usará la lógica interna para determinar la configuración si no se especifican. Este es el valor predeterminado.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Habilita las características que producirán la mejor calidad visual. Al usar este valor, se configura el códec como si hubiera establecido las siguientes propiedades:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> =-1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> =-1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Si establece cualquiera de las propiedades de la lista anterior, el valor que establezca invalidará los valores asociados a este valor, a excepción de <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Establecer el valor de la \_ propiedad MFPKEY COMPRESSIONOPTIMIZATIONTYPE en 1 también tiene el efecto de establecer el valor del registro de la opción Dquant en 2 y el valor del registro del método de costo del vector de movimiento en 1. Para obtener más información, vea el artículo Web [uso de la configuración avanzada del códec de perfil avanzado de Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




