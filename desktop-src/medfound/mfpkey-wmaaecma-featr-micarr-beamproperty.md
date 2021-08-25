---
description: Especifica qué haz usa el DSP de captura de voz para el procesamiento de la matriz de micrófonos.
ms.assetid: 9ed761da-3f1b-47e8-b71f-becc56fe8801
title: MFPKEY_WMAAECMA_FEATR_MICARR_BEAM (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b9a91cef7d270af37adc8fda9805d7bf275ef9877883ed8ff8cfdbf9e7a55e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953535"
---
# <a name="mfpkey_wmaaecma_featr_micarr_beam-property"></a>Propiedad MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ BEAM

Especifica qué haz usa el DSP de captura de voz para el procesamiento de la matriz de micrófonos.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Solo está disponible mediante [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="applies-to"></a>Se aplica a

-   [DSP de captura de voz](voicecapturedmo.md)

## <a name="remarks"></a>Comentarios

Establezca esta propiedad si el valor de la propiedad [ \_ MFPKEY WMAAECMA \_ FEATR \_ MICARR \_ MODE](mfpkey-wmaaecma-featr-micarr-modeproperty.md) es MICARRAY \_ EXTERN \_ BEAM.

Si el valor de [**MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ MODE**](mfpkey-wmaaecma-featr-micarr-modeproperty.md) es MICARRAY SINGLE BEAM, puede leer esta propiedad para consultar qué haz seleccionó \_ el \_ DSP.

Esta propiedad puede tener los siguientes valores. Los valores están en grados horizontales.



| Value | Descripción              |
|-------|--------------------------|
| 0     | -50 grados.             |
| 1     | -40 grados.             |
| 2     | -30 grados.             |
| 3     | -20 grados.             |
| 4     | -10 grados.             |
| 5     | 0 grados (haz central). |
| 6     | 10 grados.              |
| 7     | 20 grados.              |
| 8     | 30 grados.              |
| 9     | 40 grados.              |
| 10    | 50 grados.              |



 

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

 

 
