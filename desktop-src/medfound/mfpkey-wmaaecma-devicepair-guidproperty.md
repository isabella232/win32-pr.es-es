---
description: Identifica la combinación de dispositivos de audio que la aplicación usa actualmente con el DSP de captura de voz.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: MFPKEY_WMAAECMA_DEVICEPAIR_GUID propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174bbae3c83ef28ece7d05e36b0a05813078a9a9fba73ac7fae7dba25b67fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973334"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>Propiedad GUID MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_

Identifica la combinación de dispositivos de audio que la aplicación usa actualmente con el DSP de captura de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ CLSID

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

Establezca esta propiedad si usa el DSP en modo de filtro y el valor de la propiedad [ \_ MFPKEY WMAAECMA \_ RETRIEVE \_ TS \_ STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) es VARIANT \_ TRUE.

Cuando la propiedad [**\_ MFPKEY WMAAECMA \_ RETRIEVE \_ TS \_ STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) es VARIANT TRUE, el DSP recopila estadísticas sobre las marcas de tiempo de los dispositivos de audio y almacena esta información en el \_ registro. Estas estadísticas pueden cambiar para cada combinación de dispositivo de captura de audio y dispositivo de representación de audio. Por lo tanto, la aplicación debe asignar un GUID para identificar la combinación concreta de dispositivos en uso. La aplicación debe realizar un seguimiento de este GUID, de modo que pueda asignar el mismo GUID siempre que use el mismo par de dispositivos de audio.

Si usa el DSP en modo de origen, no es necesario establecer esta propiedad. El DSP genera automáticamente un GUID basado en el valor de la propiedad [ \_ MFPKEY WMAAECMA \_ DEVICE \_ INDEXES.](mfpkey-wmaaecma-device-indexesproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
