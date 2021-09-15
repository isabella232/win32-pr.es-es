---
description: Establece el número de subprocesos de trabajo que usa un descodificador de vídeo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: CODECAPI_AVDecNumWorkerThreads propiedad (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574976"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>Propiedad CODECAPI \_ AVDecNumWorkerThreads

Establece el número de subprocesos de trabajo que usa un descodificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**LONG** (**VT \_ I4**)

## <a name="property-guid"></a>GUID de propiedad

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Observaciones

Si el valor es 1, el descodificador selecciona el número de subprocesos.

Para la [**interfaz ICodecAPI,**](/windows/desktop/api/strmif/nn-strmif-icodecapi) establezca esta propiedad como **un valor LONG** **(VT \_ I4).** Para la [**interfazATTRIBUTEAttributes,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) establezca esta propiedad como **UINT32**, aunque el valor esté firmado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

