---
description: Representa una solicitud de un ejemplo de MediaStreamSource.
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
ms.openlocfilehash: a0becbcef7e71f6859a9e4f09e81f98459911724127ade97e84de09e94a956f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941925"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Interfaz IMFMediaStreamSourceSampleRequest

Representa una solicitud de un ejemplo de MediaStreamSource.

## <a name="members"></a>Miembros

La **interfaz IMFMediaStreamSourceSampleRequest** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMFMediaStreamSourceSampleRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMFMediaStreamSourceSampleRequest** tiene estos métodos.



| Método                                                           | Descripción                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Establece el ejemplo para el origen de la secuencia multimedia.<br/> |



 

## <a name="remarks"></a>Comentarios

**MFMediaStreamSourceSampleRequest** se implementa mediante el [**Windows. Clase en tiempo de ejecución Media.Core.MediaStreamSourceSampleRequest.**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                       |
| Idl<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation Interfaces](media-foundation-interfaces.md)
</dt> </dl>

 

 
