---
description: Especifica qué dispositivos de audio usa el DSP de captura de voz para capturar y representar audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: Propiedad MFPKEY_WMAAECMA_DEVICE_INDEXES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908385"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>Propiedad de los índices de dispositivo de MFPKEY \_ WMAAECMA \_ \_

Especifica qué dispositivos de audio usa el DSP de captura de voz para capturar y representar audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

(-1,-1).

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

Establezca esta propiedad si usa el DSP en modo de origen. El DSP omite esta propiedad en modo de filtro.

El valor de la propiedad es una **palabra** de 2 16 bits empaquetada en un **DWORD**. Los 16 bits superiores especifican el dispositivo de representación de audio (normalmente un orador) y los 16 bits inferiores especifican el dispositivo de captura (normalmente un micrófono). Cada dispositivo se especifica como un índice en la recopilación de dispositivos de audio. Si el índice es-1, se usa el dispositivo predeterminado.

El índice del dispositivo corresponde al índice de la colección que se usa en la interfaz [**IMMDeviceCollection**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) . La aplicación debe reproducir la voz de un extremo a través del dispositivo de representación seleccionado. (La voz de extremo final es la voz de la persona en el otro extremo de la línea de teléfono, que se reproduce a través del altavoz en el equipo del usuario). Si el dispositivo de representación seleccionado no tiene un flujo activo, el DSP no puede procesar ningún resultado.

El valor predeterminado de esta propiedad es (-1,-1).

En el ejemplo siguiente se muestra cómo inicializar **PROPVARIANT** para esta propiedad.


```
int iSpeakerIndex = -1;
int iMicrophoneIndex = -1;

// Find the device indexes to initialize iSpeakerIndex and 
// iMicrophone index (not shown).

PROPVARIANT varDeviceIndexes;
PropVariantInit(&varDeviceIndexes);
varDeviceIndexes.vt = VT_I4;
varDeviceIndexes.lVal = (unsigned long)(iSpeakerIndex << 16) + 
    (unsigned long)(0x0000ffff & iMicrophoneIndex);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
