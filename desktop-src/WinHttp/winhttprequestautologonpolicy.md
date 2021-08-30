---
description: Incluye la configuración posible de la directiva de inicio de sesión automático.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Enumeración WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: 2db50abfa413fc8ed80724ce2955407624c836a14809da678989753668794f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899085"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>Enumeración WinHttpRequestAutoLogonPolicy

La **enumeración WinHttpRequestAutoLogonPolicy** incluye la configuración posible para la [directiva de inicio de sesión automático](authentication-in-winhttp.md).

## <a name="syntax"></a>Syntax


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ Always**
</dt> <dd>

Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes.

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**
</dt> <dd>

Un inicio de sesión autenticado, con las credenciales predeterminadas, solo se realiza para las solicitudes en la intranet local. La intranet local se considera cualquier servidor de la lista de omisión de proxy en la configuración de proxy actual.

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ Never**
</dt> <dd>

La autenticación no se usa automáticamente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para establecer la directiva de inicio de sesión automático, llame al [**método SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) y especifique una de las constantes anteriores.

> [!Note]  
> Para Windows XP y Windows 2000, consulte la sección [Requisitos](winhttp-start-page.md) en tiempo de ejecución de la página de inicio de WinHTTP.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional solo con aplicaciones de escritorio sp3 \[\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server solo con aplicaciones de escritorio SP3 \[\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5.0 y Internet Explorer 5.01 o posterior en Windows XP y Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




