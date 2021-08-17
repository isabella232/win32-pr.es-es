---
description: 'MFPKEY_RESIZE_INTERLACE propiedad: especifica si el flujo de entrada está entrelazado.'
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: MFPKEY_RESIZE_INTERLACE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c614865d0c8a49238b9c8d6f7714787bb22aaadaa317a8a3a0405a7f51c87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873039"
---
# <a name="mfpkey_resize_interlace-property"></a>Propiedad MFPKEY \_ RESIZE \_ INTERLACE

Especifica si el flujo de entrada está entrelazado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="applies-to"></a>Se aplica a

-   [DSP de cambio de tamaño de vídeo](videoresizer.md)

## <a name="remarks"></a>Comentarios

Utilice uno de los valores siguientes:



| Value     | Descripción |
|-----------|-------------|
| VT \_ FALSE | progresivo |
| VT \_ TRUE  | Interlaced  |



 

Si no se establece esta propiedad, el DSP usa el tipo de medio de entrada para determinar si el vídeo está entrelazado. Puede establecer esta propiedad para invalidar la configuración del tipo de medio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
