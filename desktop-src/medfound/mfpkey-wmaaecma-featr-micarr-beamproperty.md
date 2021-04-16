---
description: Especifica el rayo que usa el DSP de la captura de voz para el procesamiento de la matriz de micrófono.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: Propiedad MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9165eec0dee87fa5d9f6a751f41e81d0de2d9958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696696"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>MFPKEY \_ WMAAECMA \_ feat \_ MICARR \_

Especifica el rayo que usa el DSP de la captura de voz para el procesamiento de la matriz de micrófono.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Observaciones

Establezca esta propiedad si el valor de la propiedad [MFPKEY \_ WMAAECMA \_ feat \_ \_ mode MICARR](mfpkey-wmaaecma-featr-micarr-modeproperty.md) es MICARRAY \_ externo \_ viga.

Si el valor del [**\_ modo MFPKEY WMAAECMA \_ featr \_ MICARR \_**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) es MICARRAY de \_ un solo \_ rayo, puede leer esta propiedad para consultar qué rayo ha seleccionado el DSP.

Esta propiedad puede tener los valores siguientes. Los valores están en horizontal.



| Value | Descripción              |
|-------|--------------------------|
| 0     | -50 grados.             |
| 1     | -40 grados.             |
| 2     | -30 grados.             |
| 3     | -20 grados.             |
| 4     | -10 grados.             |
| 5     | 0 grados (centro). |
| 6     | 10 grados.              |
| 7     | 20 grados.              |
| 8     | 30 grados.              |
| 9     | 40 grados.              |
| 10    | 50 grados.              |



 

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

 

 
