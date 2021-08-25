---
description: El método get ProtocolVersion obtiene la versión del protocolo del Protocolo de descriptor de \_ sesión (SDP; vea RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: Método ITSdp::get_ProtocolVersion (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54bd664a2a1147b341d46a83c4a2fa72c66585a11fc8eaef154aa213cab8945
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774495"
---
# <a name="itsdpget_protocolversion-method"></a>ItSdp::get \_ ProtocolVersion (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ ProtocolVersion** obtiene la versión del protocolo del Protocolo de descriptor de sesión (SDP; vea RFC 2327).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProtocolVersion* \[ out\]
</dt> <dd>

Puntero a la versión del protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                        |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pProtocolVersion* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




