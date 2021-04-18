---
description: Establece el número de subprocesos de trabajo usados por un descodificador de vídeo.
ms.assetid: A1570BB5-62BC-46C0-B9C9-61F99AA13BBE
title: Propiedad CODECAPI_AVDecNumWorkerThreads (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d7c57d1b4176ad65313a5583a70f9ba4f7427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714938"
---
# <a name="codecapi_avdecnumworkerthreads-property"></a>\_Propiedad AVDecNumWorkerThreads de CODECAPI

Establece el número de subprocesos de trabajo usados por un descodificador de vídeo.

## <a name="data-type"></a>Tipo de datos

**Long** (**VT \_ I4**)

## <a name="property-guid"></a>GUID de propiedad

CODECAPI \_ AVDecNumWorkerThreads

## <a name="remarks"></a>Observaciones

Si el valor es 1, el descodificador selecciona el número de subprocesos.

Para la interfaz [**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi) , establezca esta propiedad como un valor **Long** (**VT \_ I4**). Para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , establezca esta propiedad como **UINT32**, aunque el valor es signed.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

