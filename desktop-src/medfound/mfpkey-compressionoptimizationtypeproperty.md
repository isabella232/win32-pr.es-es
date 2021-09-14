---
description: Especifica la configuración de calidad visual óptima que se usará para el codificador Windows advanced Profile de Media Video 9.
ms.assetid: 9449b5fa-4f13-4c33-bfdf-611720e8dd77
title: MFPKEY_COMPRESSIONOPTIMIZATIONTYPE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e140a854999a5c634620d98958e40832acbe9439
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127257695"
---
# <a name="mfpkey_compressionoptimizationtype-property"></a>Propiedad MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE

Especifica la configuración de calidad visual óptima que se usará para el codificador Windows advanced Profile de Media Video 9.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCCompressionOptimizationType

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

0

## <a name="remarks"></a>Observaciones

Esta propiedad proporciona una manera rápida de configurar una serie de opciones de codificación de vídeo. Se puede establecer en uno de los valores siguientes.




| Value | Descripción | 
|-------|-------------|
| 0 | El códec no forzará la optimización y usará las características especificadas por otras propiedades. En muchos casos, el códec usará lógica interna para determinar la configuración si no se especifican. Este es el valor predeterminado. | 
| 1 | Habilita las características que producirán la mejor calidad visual. Con este valor se configura el códec como si hubiera establecido las siguientes propiedades:<br /><ul><li><a href="mfpkey-bdeltaqpproperty.md">MFPKEY_BDELTAQP</a> = 1</li><li><a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a> = 3</li><li><a href="mfpkey-loopfilterproperty.md">MFPKEY_LOOPFILTER</a> = 1</li><li><a href="mfpkey-motionmatchmethodproperty.md">MFPKEY_MOTIONMATCHMETHOD</a> = -1</li><li><a href="mfpkey-motionsearchlevelproperty.md">MFPKEY_MOTIONSEARCHLEVEL</a> = 1</li><li><a href="mfpkey-motionsearchrangeproperty.md">MFPKEY_MOTIONSEARCHRANGE</a> = -1</li><li><a href="mfpkey-numbframesproperty.md">MFPKEY_NUMBFRAMES</a> = 1</li></ul>Si establece cualquiera de las propiedades de la lista anterior, el valor establecido invalida los valores asociados a esta configuración, excepto <a href="mfpkey-complexityexproperty.md">MFPKEY_COMPLEXITYEX</a>.<br /> | 




 

Establecer el valor de la propiedad MFPKEY COMPRESSIONOPTIMIZATIONTYPE en 1 también tiene el efecto de establecer la configuración del Registro Dquant Option en 2 y la opción del Registro Motion Vector Cost Method en \_ 1. Para obtener más información, vea el artículo web Uso de la Configuración advanced Windows Media Video 9 Advanced Profile Codec ( Códec de perfil [avanzado de Media Video 9).](https://www.microsoft.com/windows/windowsmedia/howto/articles/codecadvancedsettings.aspx)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




