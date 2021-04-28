---
description: 'MFPKEY_COLORCONV_MODE propiedad : especifica si el flujo de entrada está entrelazado.'
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: MFPKEY_COLORCONV_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8c3f2d6256c4d7a9410264fb18703eea251e9c6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087583"
---
# <a name="mfpkey_colorconv_mode-property"></a>Propiedad MFPKEY \_ COLORCONV \_ MODE

Especifica si el flujo de entrada está entrelazado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

Calculado por el DSP del vídeo de origen.

## <a name="applies-to"></a>Se aplica a

-   [DSP del convertidor de colores](colorconverter.md)

## <a name="remarks"></a>Comentarios

Use uno de los siguientes valores.



| Valor | Descripción |
|-------|-------------|
| 0     | progresivo |
| 2     | Interlaced  |



 

Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado. Puede establecer esta propiedad para invalidar la configuración del tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
