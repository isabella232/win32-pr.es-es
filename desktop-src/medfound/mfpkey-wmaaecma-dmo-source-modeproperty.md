---
description: Especifica si el DSP de la captura de voz usa el modo de origen o el modo de filtro.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Propiedad MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275856"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>Propiedad del modo de origen de MFPKEY \_ WMAAECMA \_ DMO \_ \_

Especifica si el DSP de la captura de voz usa el modo de origen o el modo de filtro.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ bool

## <a name="default-value"></a>Valor predeterminado

VARIANTE \_ true

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

En el modo de origen, la aplicación no tiene que enviar datos de entrada al DSP, porque el DSP extrae automáticamente los datos de los dispositivos de audio. En el modo de filtro, la aplicación debe enviar los datos de entrada al DSP.

Esta propiedad puede tener los valores siguientes.



| Value          | Descripción  |
|----------------|--------------|
| VARIANTE \_ false | Modo de filtro. |
| VARIANTE \_ true  | Modo de origen. |



 

> [!Note]  
> Cuando DMO está en modo de origen, solo debe llamar a [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) para establecer el formato del flujo de salida y no llamar a [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) para establecer formatos de flujo de entrada. De lo contrario, se producirá un error al inicializar DMO

 

Si el valor de esta propiedad es VARIANT \_ true, el DSP tiene cero entradas. Si el valor es VARIANT \_ false, el DSP tiene una o dos entradas, dependiendo del valor de la propiedad [MFPKEY \_ WMAAECMA \_ del \_ modo del sistema](mfpkey-wmaaecma-system-modeproperty.md) , como se muestra en la tabla siguiente.



| Value                     | Número de entradas |
|---------------------------|------------------|
| \_matriz OPTIBEAM \_ y \_ AEC | 2                |
| \_solo matriz \_ OPTIBEAM     | 1                |
| \_AEC de canal único \_      | 2                |
| \_NSAGC de canal único \_    | 1                |



 

> [!Note]  
> Solo los modos con una sola entrada funcionarán con el filtro de contenedor DMO de la API de DirectShow 9,0.

 

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

 

 
