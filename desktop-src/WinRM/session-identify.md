---
title: Método Session.Identify (WSManDisp.h)
description: Consulta un equipo remoto para determinar si admite el protocolo WS-Management usuario.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identificación del método Windows administración remota
- Identificar métodos Windows administración remota , objeto session
- Session object Windows Remote Management , Identify method
topic_type:
- apiref
api_name:
- Session.Identify
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e897a82644fec7bf206e99ea87ae2df82793a9717259b76fd9ca9d264c74f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642555"
---
# <a name="sessionidentify-method"></a>Método Session.Identify

El **método Session.Identify** consulta un equipo remoto para determinar si admite WS-Management protocolo. Para obtener más información, vea [Detectar si un equipo remoto admite WS-Management protocolo](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Sintaxis


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*flags* \[ in, opcional\]
</dt> <dd>

Para enviar la solicitud en modo autenticado, use la constante de autenticación de la **enumeración WSManSessionFlags.** Para enviar en modo no autenticado, use **WSManFlagUseNoAuthentication**. Para obtener más información, vea [**Constantes de autenticación**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena XML que especifica la versión del protocolo WS-Management, el proveedor del sistema operativo y, si se envió la solicitud autenticada, la versión del sistema operativo.

## <a name="remarks"></a>Comentarios

**Session.Identify** se basa en la [protocolo WS-Management](ws-management-protocol.md) definida como wsmanIdentity. Esto se especifica en el paquete SOAP como se indica a continuación:


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de VBScript se envía una solicitud de identificación no autenticada al equipo remoto denominado Remoto en el mismo dominio.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Sesión**](session.md)
</dt> <dt>

[**IWSManSession::Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

 





