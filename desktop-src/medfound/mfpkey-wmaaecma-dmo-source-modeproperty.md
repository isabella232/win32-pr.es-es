---
description: Especifica si el DSP de captura de voz usa el modo de origen o el modo de filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: MFPKEY_WMAAECMA_DMO_SOURCE_MODE propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec9dd01be5a020047410362b2fdfc27fd8d703a393e3ae2f557b1dd3a42bf80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555305"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE

Especifica si el DSP de captura de voz usa el modo de origen o el modo de filtro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ BOOL

## <a name="default-value"></a>Valor predeterminado

VARIANT \_ TRUE

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

En el modo de origen, la aplicación no necesita enviar datos de entrada al DSP, ya que este extrae automáticamente los datos de los dispositivos de audio. En el modo de filtro, la aplicación debe enviar los datos de entrada al DSP.

Esta propiedad puede tener los siguientes valores.



| Value          | Descripción  |
|----------------|--------------|
| VARIANT \_ FALSE | Modo de filtro. |
| VARIANT \_ TRUE  | Modo de origen. |



 

> [!Note]  
> Cuando el DMO está en modo de origen, solo debe llamar a [**IMediaObject::SetOutputType para**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) establecer el formato del flujo de salida y no llamar a [**IMediaObject::SetInputType para**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) establecer los formatos de flujo de entrada. De lo DMO se producirá un error en la inicialización.

 

Si el valor de esta propiedad es VARIANT \_ TRUE, el DSP tiene cero entradas. Si el valor es VARIANT FALSE, el DSP tiene una o dos entradas, dependiendo del valor de la propiedad \_ [MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE,](mfpkey-wmaaecma-system-modeproperty.md) como se muestra en la tabla siguiente.



| Value                     | Número de entradas |
|---------------------------|------------------|
| OPTIBEAM \_ ARRAY \_ Y \_ AEC | 2                |
| OPTIBEAM ARRAY ONLY (SOLO \_ MATRIZ DE OPTIBEAM) \_     | 1                |
| AEC \_ \_ DE CANAL ÚNICO      | 2                |
| \_ \_ NSAGC DE CANAL ÚNICO    | 1                |



 

> [!Note]  
> Solo los modos con una sola entrada funcionarán con el filtro de DMO de la API DirectShow 9.0.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 
