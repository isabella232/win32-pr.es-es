---
title: Constantes y enumeraciones de WinRM
description: Administración remota de Windows tiene marcas de bits usadas en la creación de sesiones y enumeraciones, y para los tipos de acceso y la autenticación en un servidor proxy.
ms.assetid: 17e59245-26a3-4383-a741-4a09f3cfcec6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0789d440ff0f88cc037e0dc9e544ca559c1af5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076025"
---
# <a name="winrm-constants-and-enumerations"></a><span data-ttu-id="375c6-103">Constantes y enumeraciones de WinRM</span><span class="sxs-lookup"><span data-stu-id="375c6-103">WinRM Constants and Enumerations</span></span>

<span data-ttu-id="375c6-104">Administración remota de Windows tiene marcas de bits usadas en la creación de sesiones y enumeraciones, y para los tipos de acceso y la autenticación en un servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="375c6-104">Windows Remote Management has bit flags used in creating sessions and enumerations, and for access types and authentication to a proxy server.</span></span> <span data-ttu-id="375c6-105">En la lista siguiente se enumeran las diferentes marcas de bits.</span><span class="sxs-lookup"><span data-stu-id="375c6-105">The following list lists the different bit flags.</span></span>

<dl> <dt>

<span data-ttu-id="375c6-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Constantes de sesión](session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="375c6-106"><span id="Session_Constants"></span><span id="session_constants"></span><span id="SESSION_CONSTANTS"></span>[Session Constants](session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="375c6-107">Marcas usadas en el parámetro *Flags* de los métodos [**WSMan. createSession**](wsman-createsession.md) o [**IWSMan:: createSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) .</span><span class="sxs-lookup"><span data-stu-id="375c6-107">Flags used in *flags* parameter of the [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) methods.</span></span>

</dd> <dt>

<span data-ttu-id="375c6-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Constantes de enumeración**](enumeration-constants.md)</span><span class="sxs-lookup"><span data-stu-id="375c6-108"><span id="Enumeration_Constants"></span><span id="enumeration_constants"></span><span id="ENUMERATION_CONSTANTS"></span>[**Enumeration Constants**](enumeration-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="375c6-109">Marcas usadas en el parámetro *Flags* de Call to [**Session. Enumerate**](session-enumerate.md) o [**IWSManSession:: Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span><span class="sxs-lookup"><span data-stu-id="375c6-109">Flags used in *flags* parameter of call to [**Session.Enumerate**](session-enumerate.md) or [**IWSManSession::Enumerate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-enumerate).</span></span>

</dd> <dt>

<span data-ttu-id="375c6-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span><span class="sxs-lookup"><span data-stu-id="375c6-110"><span id="WSManProxyAuthenticationFlags"></span><span id="wsmanproxyauthenticationflags"></span><span id="WSMANPROXYAUTHENTICATIONFLAGS"></span>[**WSManProxyAuthenticationFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyauthenticationflags)</span></span>
</dt> <dd>

<span data-ttu-id="375c6-111">Marcas usadas en el parámetro *authenticationMechanism* de la llamada a [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span><span class="sxs-lookup"><span data-stu-id="375c6-111">Flags used in *authenticationMechanism* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> <dt>

<span data-ttu-id="375c6-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span><span class="sxs-lookup"><span data-stu-id="375c6-112"><span id="WSManProxyAccessTypeFlags"></span><span id="wsmanproxyaccesstypeflags"></span><span id="WSMANPROXYACCESSTYPEFLAGS"></span>[**WSManProxyAccessTypeFlags**](/windows/desktop/api/WSManDisp/ne-wsmandisp-wsmanproxyaccesstypeflags)</span></span>
</dt> <dd>

<span data-ttu-id="375c6-113">Marcas usadas en el parámetro *accessType* de la llamada a [**IWSManConnectionOptionsEx2:: SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span><span class="sxs-lookup"><span data-stu-id="375c6-113">Flags used in *accessType* parameter of call to [**IWSManConnectionOptionsEx2::SetProxy**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="375c6-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="375c6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="375c6-115">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="375c6-115">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dt>

[<span data-ttu-id="375c6-116">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="375c6-116">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="375c6-117">**IWSMan:: CreateSession**</span><span class="sxs-lookup"><span data-stu-id="375c6-117">**IWSMan::CreateSession**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession)
</dt> <dt>

[<span data-ttu-id="375c6-118">**IWSManConnectionOptionsEx2:: SetProxy**</span><span class="sxs-lookup"><span data-stu-id="375c6-118">**IWSManConnectionOptionsEx2::SetProxy**</span></span>](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanconnectionoptionsex2-setproxy)
</dt> </dl>

 

 




