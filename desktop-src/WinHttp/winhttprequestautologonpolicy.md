---
description: Incluye posibles valores para la Directiva de inicio de sesión automático.
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
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715160"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a>Enumeración WinHttpRequestAutoLogonPolicy

La enumeración **WinHttpRequestAutoLogonPolicy** incluye posibles valores para la [Directiva de inicio de sesión automático](authentication-in-winhttp.md).

## <a name="syntax"></a>Sintaxis


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ siempre**
</dt> <dd>

Se realiza un inicio de sesión autenticado con las credenciales predeterminadas para todas las solicitudes.

</dd> <dt>

<span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**
</dt> <dd>

Un inicio de sesión autenticado, con las credenciales predeterminadas, solo se realiza para las solicitudes en la Intranet local. La Intranet local se considera cualquier servidor de la lista de omisión de proxy en la configuración del proxy actual.

</dd> <dt>

<span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ nunca**
</dt> <dd>

La autenticación no se utiliza automáticamente.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para establecer la Directiva de inicio de sesión automático, llame al método [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) y especifique una de las constantes anteriores.

> [!Note]  
> En Windows XP y Windows 2000, consulte la sección [requisitos de tiempo de ejecución](winhttp-start-page.md) de la página de inicio de winhttp.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP, Windows 2000 Professional con las \[ aplicaciones de escritorio de SP3 únicamente\]<br/>            |
| Servidor mínimo compatible<br/> | Windows Server 2003, Windows 2000 Server con \[ solo aplicaciones de escritorio de SP3\]<br/>         |
| Redistribuible<br/>          | WinHTTP 5,0 e Internet Explorer 5,01 o posterior en Windows XP y Windows 2000.<br/> |
| IDL<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Versiones de WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




