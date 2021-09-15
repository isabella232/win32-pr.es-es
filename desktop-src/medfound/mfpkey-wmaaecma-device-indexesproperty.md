---
description: Especifica qué dispositivos de audio usa el DSP de captura de voz para capturar y representar audio.
ms.assetid: 42b6b82b-ac64-4a07-956c-473dd57a128d
title: MFPKEY_WMAAECMA_DEVICE_INDEXES propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b377e4335e78e81c8e7d3c5a9a0c1d00b8f9bae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468619"
---
# <a name="mfpkey_wmaaecma_device_indexes-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ DEVICE \_ INDEXES

Especifica qué dispositivos de audio usa el DSP de captura de voz para capturar y representar audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

(-1, -1).

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

Establezca esta propiedad si usa el DSP en modo de origen. El DSP omite esta propiedad en modo de filtro.

El valor de la propiedad es dos word **de** 16 bits empaquetados en **un DWORD**. Los 16 bits superiores especifican el dispositivo de representación de audio (normalmente un altavoz) y los 16 bits inferiores especifican el dispositivo de captura (normalmente un micrófono). Cada dispositivo se especifica como un índice en la colección de dispositivos de audio. Si el índice es -1, se usa el dispositivo predeterminado.

El índice de dispositivo corresponde al índice de recopilación usado en la [**interfaz IMMDeviceCollection.**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevicecollection) La aplicación debe reproducir la voz de extremo a través del dispositivo de representación seleccionado. (La voz de extremo a extremo es la voz de la persona en el otro extremo de la línea telefónica, que se reproduce a través del hablante en el equipo del usuario). Si el dispositivo de representación seleccionado no tiene una secuencia activa, el DSP no puede procesar ninguna salida.

El valor predeterminado de esta propiedad es (-1, -1).

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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[DSP de captura de voz](voicecapturedmo.md)
</dt> </dl>

 

 
