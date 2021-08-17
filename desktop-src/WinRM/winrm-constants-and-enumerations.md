---
title: Constantes y enumeraciones de WinRM
description: Windows Administración remota tiene marcas de bits usadas en la creación de sesiones y enumeraciones, así como para los tipos de acceso y la autenticación en un servidor proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73de8f418d5b0fb0bd7adebb8439ccbce67f0bcb6aacf72ed2665683c00e0076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742941"
---
# <a name="winrm-constants-and-enumerations"></a>Constantes y enumeraciones de WinRM

Windows Administración remota tiene marcas de bits usadas en la creación de sesiones y enumeraciones, así como para los tipos de acceso y la autenticación en un servidor proxy. En la lista siguiente se enumeran las distintas marcas de bits.

<dl> <dt>

<span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Constantes de sesión](session-constants.md)
</dt> <dd>

Marcas usadas en *el parámetro flags* de los [**métodos WSMan.CreateSession**](wsman-createsession.md) [**o IWSMan::CreateSession.**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)

</dd> <dt>

<span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Constantes de enumeración**](enumeration-constants.md)
</dt> <dd>

Marcas usadas en *el parámetro flags* de la llamada a [**Session.Enumerate**](session-enumerate.md) [**o IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).

</dd> <dt>

<span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)
</dt> <dd>

Marcas usadas en el *parámetro authenticationMechanism* de la llamada [**a IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> <dt>

<span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)
</dt> <dd>

Marcas usadas en el *parámetro accessType* de la llamada [**a IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> <dt>

[**WSMan.CreateSession**](wsman-createsession.md)
</dt> <dt>

[**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




