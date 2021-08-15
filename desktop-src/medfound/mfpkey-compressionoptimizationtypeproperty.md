---
description: Especifica la configuración de calidad visual óptima que se usará para el codificador Windows advanced Profile de Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7171990280fe004b12c306a09af3b617ba2de0a7cfa274edb3d9191b16a886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118242884"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>Propiedad MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE

Especifica la configuración de calidad visual óptima que se usará para el codificador Windows advanced Profile de Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Comentarios

Esta propiedad proporciona una manera rápida de configurar una serie de opciones de codificación de vídeo. Se puede establecer en uno de los valores siguientes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>El códec no forzará la optimización y usará las características especificadas por otras propiedades. En muchos casos, el códec usará lógica interna para determinar la configuración si no se especifican. Este es el valor predeterminado.</td>
</tr>
<tr class="even">
<td>1</td>
<td>Habilita las características que producirán la mejor calidad visual. Con este valor se configura el códec como si hubiera establecido las siguientes propiedades:<br/>
<ul>
<li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li>
<li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li>
<li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li>
<li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li>
<li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li>
<li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li>
<li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li>
</ul>
Si establece cualquiera de las propiedades de la lista anterior, el valor establecido invalida los valores asociados a esta configuración, excepto <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br/></td>
</tr>
</tbody>
</table>



 

Establecer el valor de la propiedad MFPKEY COMPRESSIONOPTIMIZATIONTYPE en 1 también tiene el efecto de establecer la configuración del Registro Dquant Option en 2 y la opción del Registro Motion Vector Cost Method en \_ 1. Para obtener más información, vea el artículo web Uso de advanced Configuración del códec de perfil avanzado [Windows Media Video 9](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




