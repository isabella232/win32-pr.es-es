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
ms.openlocfilehash: fa159727c6e13a894148391b9508afad4b8dacfc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474253"
---
# <a name="imfmediastreamsourcesamplerequest-interface"></a>Interfaz IMFMediaStreamSourceSampleRequest

Representa una solicitud de un ejemplo de MediaStreamSource.

## <a name="members"></a>Members

La **interfaz IMFMediaStreamSourceSampleRequest** hereda de [**la interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMFMediaStreamSourceSampleRequest** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IMFMediaStreamSourceSampleRequest** tiene estos métodos.



| Método                                                           | Descripción                                             |
|:-----------------------------------------------------------------|:--------------------------------------------------------|
| [**SetSample**](imfmediastreamsourcesamplerequest-setsample.md) | Establece el ejemplo para el origen del flujo multimedia.<br/> |



 

## <a name="remarks"></a>Observaciones

**MFMediaStreamSourceSampleRequest** se implementa mediante el [**Windows. Clase en tiempo de ejecución Media.Core.MediaStreamSourceSampleRequest.**](/uwp/api/Windows.Media.Core.MediaStreamSourceSampleRequest?view=winrt-19041)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Mfidl.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation Interfaces](media-foundation-interfaces.md)
</dt> </dl>

 

 
