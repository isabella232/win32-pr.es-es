---
title: IMsTscAxEvents OnRemoteProgramResult, método
description: Se llama cuando un programa RemoteApp devuelve un resultado al control de cliente.
ms.assetid: 5bc9570f-14fb-4b6f-a7dd-c1bce3ef19e0
ms.tgt_platform: multiple
keywords:
- Método OnRemoteProgramResult Servicios de Escritorio remoto
- Método OnRemoteProgramResult Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnRemoteProgramResult
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteProgramResult
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 880e4fb3f6453114415f5bcc07a0afb9c176a1bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150497"
---
# <a name="imstscaxeventsonremoteprogramresult-method"></a>IMsTscAxEvents:: OnRemoteProgramResult (método)

Se llama cuando un programa RemoteApp devuelve un resultado al control de cliente.

## <a name="syntax"></a>Sintaxis


```C++
VOID OnRemoteProgramResult(
  [in] BSTR                bstrRemoteProgram,
  [in] RemoteProgramResult lError,
  [in] VARIANT_BOOL        vbIsExecutable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrRemoteProgram* \[ de\]
</dt> <dd>

Nombre del programa RemoteApp.

</dd> <dt>

*lError* \[ de\]
</dt> <dd>

El resultado del intento de iniciar el programa RemoteApp.

<dt>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>

<span id="remoteAppResultOk"></span><span id="remoteappresultok"></span><span id="REMOTEAPPRESULTOK"></span>**remoteAppResultOk** (0 (0X0))


</dt> <dd>

El programa RemoteApp se inició correctamente.

</dd> <dt>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>

<span id="remoteAppResultLocked"></span><span id="remoteappresultlocked"></span><span id="REMOTEAPPRESULTLOCKED"></span>**remoteAppResultLocked** (1 (0x1))


</dt> <dd>

La sesión remota está bloqueada y no se puede iniciar el programa RemoteApp. El usuario debe escribir sus credenciales para desbloquear la sesión y, a continuación, iniciar el programa RemoteApp.

</dd> <dt>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>

<span id="remoteAppResultProtocolError"></span><span id="remoteappresultprotocolerror"></span><span id="REMOTEAPPRESULTPROTOCOLERROR"></span>**remoteAppResultProtocolError** (2 (0X2))


</dt> <dd>

El programa RemoteApp devolvió un error de protocolo.

</dd> <dt>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>

<span id="remoteAppResultNotInWhitelist"></span><span id="remoteappresultnotinwhitelist"></span><span id="REMOTEAPPRESULTNOTINWHITELIST"></span>**remoteAppResultNotInWhitelist** (3 (0X3))


</dt> <dd>

El programa RemoteApp no está en la lista aprobada del servidor host de sesión de escritorio remoto.

</dd> <dt>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>

<span id="remoteAppResultNetworkPathDenied"></span><span id="remoteappresultnetworkpathdenied"></span><span id="REMOTEAPPRESULTNETWORKPATHDENIED"></span>**remoteAppResultNetworkPathDenied** (4 (0x4))


</dt> <dd>

Se denegó la ruta de acceso de red al programa RemoteApp.

</dd> <dt>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>

<span id="remoteAppResultFileNotFound"></span><span id="remoteappresultfilenotfound"></span><span id="REMOTEAPPRESULTFILENOTFOUND"></span>**remoteAppResultFileNotFound** (5 (0X5))


</dt> <dd>

No se encontró el archivo de programa RemoteApp.

</dd> <dt>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>

<span id="remoteAppResultFailure"></span><span id="remoteappresultfailure"></span><span id="REMOTEAPPRESULTFAILURE"></span>**remoteAppResultFailure** (6 (0x6))


</dt> <dd>

No se pudo iniciar el programa RemoteApp.

</dd> <dt>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>

<span id="remoteAppResultHookNotLoaded"></span><span id="remoteappresulthooknotloaded"></span><span id="REMOTEAPPRESULTHOOKNOTLOADED"></span>**remoteAppResultHookNotLoaded** (7 (0X7))


</dt> <dd>

No se puede iniciar el programa RemoteApp porque la sesión muestra actualmente el escritorio seguro.

</dd> </dl> </dd> <dt>

*vbIsExecutable* \[ de\]
</dt> <dd>

Indica si el programa RemoteApp se inició directamente, utilizando el nombre del archivo ejecutable o indirectamente, mediante una asociación de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Implemente este método en el receptor de eventos para recibir la notificación de que un programa RemoteApp devolvió un resultado.

Se llama a este método inmediatamente después de que el control ActiveX intente iniciar el programa RemoteApp, y el parámetro *lError* indica el resultado del intento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





