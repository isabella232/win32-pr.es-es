---
description: Representa una solicitud para un ejemplo de un MediaStreamSource.
ms.assetid: 43617cda-84b1-405f-8a20-be793413c186
title: Interfaz IMFMediaStreamSourceSampleRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361901"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Interfaz IMFMediaStreamSourceSampleRequest

Representa una solicitud para un ejemplo de un MediaStreamSource.

## <a name="members"></a>Miembros

La interfaz **IMFMediaStreamSourceSampleRequest** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMFMediaStreamSourceSampleRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IMFMediaStreamSourceSampleRequest** tiene estos métodos.



| Método                                                           | Descripción                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Establece el ejemplo para el origen de la secuencia de medios.<br/> |



 

## <a name="remarks"></a>Observaciones

La clase de tiempo de ejecución de [**Windows. Media. Core. MediaStreamSourceSampleRequest**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041) implementa **MFMediaStreamSourceSampleRequest** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
