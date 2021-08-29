---
description: Establece el número de subprocesos de trabajo que usa un descodificador de vídeo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a17584e9a6e3d6f8efcfcf129a89bc0f94cb2629c0f130549a73757c20368f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035363"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>Propiedad CODECAPI \_ AVDecNumWorkerThreads

Establece el número de subprocesos de trabajo que usa un descodificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**LONG** (**VT \_ I4**)

## <a name="property-guid"></a>GUID de propiedad

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Comentarios

Si el valor es 1, el descodificador selecciona el número de subprocesos.

Para la [**interfaz ICodecAPI,**](/windows/desktop/api/strmif/nn-strmif-icodecapi) establezca esta propiedad como **un valor LONG** **(VT \_ I4).** Para la [**interfaz IMFAttributes,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) establezca esta propiedad como **UINT32**, aunque el valor esté firmado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

