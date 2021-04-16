---
description: El \_ método get ProtocolVersion obtiene la versión del protocolo del Protocolo de descriptor de sesión (SDP; consulte RFC 2327).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'Método ITSdp:: get_ProtocolVersion (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679492"
---
# <a name="itsdpget_protocolversion-method"></a>ITSdp:: get \_ ProtocolVersion (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ ProtocolVersion** obtiene la versión del protocolo del Protocolo de descriptor de sesión (SDP; consulte RFC 2327).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProtocolVersion* \[ enuncia\]
</dt> <dd>

Puntero a la versión del protocolo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                        |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pProtocolVersion* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>     |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                       |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




