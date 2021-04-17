---
title: Método Session. Identify (WSManDisp. h)
description: Consulta un equipo remoto para determinar si es compatible con el protocolo de WS-Management.
ms.assetid: b86ec9b8-8fc4-4c3e-aca7-2f7d039749df
ms.tgt_platform: multiple
keywords:
- Identificar método Administración remota de Windows
- Identificar Administración remota de Windows de método, objeto de sesión
- Objeto de sesión Administración remota de Windows, método de identificación
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
ms.openlocfilehash: 24f1caa5b1e44e4ca65082e33bca4d045e487c96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714629"
---
# <a name="sessionidentify-method"></a>Session. Identify (método)

El método **Session. Identify** consulta un equipo remoto para determinar si es compatible con el protocolo de WS-Management. Para obtener más información, consulte [detectar si un equipo remoto admite WS-Management protocolo](detecting-whether-a-remote-computer-supports-ws-management-protocol.md).

## <a name="syntax"></a>Sintaxis


```VB
Session.Identify( _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*marcas* \[ de en, opcional\]
</dt> <dd>

Para enviar la solicitud en modo autenticado, use la constante de autenticación de la enumeración **WSManSessionFlags** . Para enviar en modo no autenticado, use **WSManFlagUseNoAuthentication**. Para obtener más información, consulte [**constantes de autenticación**](authentication-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena XML que especifica la versión del protocolo WS-Management, el proveedor del sistema operativo y, si la solicitud se envió autenticada, la versión del sistema operativo.

## <a name="remarks"></a>Observaciones

**Session. Identify** se basa en la operación [protocolo WS-Management](ws-management-protocol.md) definida como wsmanIdentity. Esto se especifica en el paquete SOAP de la siguiente manera:


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



## <a name="examples"></a>Ejemplos

El siguiente ejemplo de VBScript envía una solicitud de identificación no autenticada al equipo remoto denominado remoto en el mismo dominio.


```VB
set WSMan = CreateObject("Wsman.Automation")
set Session = WSMan.CreateSession("Remote", _
  WSMan.SessionFlagUseNoAuthentication)
WScript.Echo Session.Identify
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**De sesión**](session.md)
</dt> <dt>

[**IWSManSession:: Identify**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify)
</dt> <dt>

[Protocolo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

 





