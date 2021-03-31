---
description: Especifica si el flujo de entrada está entrelazado.
ms.assetid: d0d93151-5b0d-44a7-8497-f11b3e23a031
title: Propiedad MFPKEY_COLORCONV_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dd8c01a6dce595eb270b734947492deea014259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812770"
---
# <a name="mfpkey_colorconv_mode-property"></a>\_Propiedad de modo COLORCONV de MFPKEY \_

Especifica si el flujo de entrada está entrelazado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

Lo calcula el DSP desde el vídeo de origen.

## <a name="applies-to"></a>Se aplica a

-   [DSP de convertidor de colores](colorconverter.md)

## <a name="remarks"></a>Observaciones

Use uno de los siguientes valores.



| Value | Descripción |
|-------|-------------|
| 0     | progresivo |
| 2     | Interlaced  |



 

Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado. Puede establecer esta propiedad para invalidar la configuración de tipo de medio.

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

 

 
