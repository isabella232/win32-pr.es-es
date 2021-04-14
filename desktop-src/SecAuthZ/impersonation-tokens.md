---
description: Explica el uso de tokens de suplantación en el control de acceso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Tokens de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668399"
---
# <a name="impersonation-tokens"></a><span data-ttu-id="3214c-103">Tokens de suplantación</span><span class="sxs-lookup"><span data-stu-id="3214c-103">Impersonation Tokens</span></span>

<span data-ttu-id="3214c-104">Un subproceso de suplantación tiene dos [*tokens de acceso*](/windows/desktop/SecGloss/a-gly):</span><span class="sxs-lookup"><span data-stu-id="3214c-104">An impersonating thread has two [*access tokens*](/windows/desktop/SecGloss/a-gly):</span></span>

-   <span data-ttu-id="3214c-105">Un [*token de acceso principal*](/windows/desktop/SecGloss/p-gly) que describe el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) del servidor.</span><span class="sxs-lookup"><span data-stu-id="3214c-105">A [*primary access token*](/windows/desktop/SecGloss/p-gly) that describes the [*security context*](/windows/desktop/SecGloss/s-gly) of the server.</span></span> <span data-ttu-id="3214c-106">Para obtener un identificador de este token, llame a la función [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .</span><span class="sxs-lookup"><span data-stu-id="3214c-106">To get a handle to this token, call the [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) function.</span></span>
-   <span data-ttu-id="3214c-107">Token de acceso de suplantación que describe el contexto de seguridad del cliente que se va a suplantar.</span><span class="sxs-lookup"><span data-stu-id="3214c-107">An impersonation access token that describes the security context of the client being impersonated.</span></span> <span data-ttu-id="3214c-108">Para obtener un identificador de este token, llame a la función [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .</span><span class="sxs-lookup"><span data-stu-id="3214c-108">To get a handle to this token, call the [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) function.</span></span>

<span data-ttu-id="3214c-109">Un servidor puede utilizar el [*token de suplantación*](/windows/desktop/SecGloss/i-gly) en las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="3214c-109">A server can use the [*impersonation token*](/windows/desktop/SecGloss/i-gly) in the following functions:</span></span>

-   <span data-ttu-id="3214c-110">En las funciones [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)y [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar si un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) permite al cliente un conjunto de derechos de acceso.</span><span class="sxs-lookup"><span data-stu-id="3214c-110">In the [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype), and [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) functions to determine whether a [*security descriptor*](/windows/desktop/SecGloss/s-gly) allows the client a set of access rights.</span></span>
-   <span data-ttu-id="3214c-111">En la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar o deshabilitar los privilegios del cliente.</span><span class="sxs-lookup"><span data-stu-id="3214c-111">In the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable or disable the client's privileges.</span></span>
-   <span data-ttu-id="3214c-112">En la función [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar si un conjunto de privilegios está habilitado en el token del cliente.</span><span class="sxs-lookup"><span data-stu-id="3214c-112">In the [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) function to determine whether a set of privileges are enabled in the client's token.</span></span>
-   <span data-ttu-id="3214c-113">En las funciones que generan entradas en el registro de eventos de seguridad, como [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) o [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span><span class="sxs-lookup"><span data-stu-id="3214c-113">In functions that generate entries in the security event log, such as [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) or [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma).</span></span> <span data-ttu-id="3214c-114">Estas funciones usan un token de suplantación para obtener información sobre el cliente para la entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="3214c-114">These functions use an impersonation token to get information about the client for the log entry.</span></span>

 

 
