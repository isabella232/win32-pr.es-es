---
description: La cuenta NetworkService es una cuenta local predefinida utilizada por el administrador de control de servicios.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Cuenta NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668293"
---
# <a name="networkservice-account"></a><span data-ttu-id="18dd5-103">Cuenta NetworkService</span><span class="sxs-lookup"><span data-stu-id="18dd5-103">NetworkService Account</span></span>

<span data-ttu-id="18dd5-104">La cuenta NetworkService es una cuenta local predefinida utilizada por el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="18dd5-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="18dd5-105">El subsistema de seguridad no reconoce esta cuenta, por lo que no puede especificar su nombre en una llamada a la función [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .</span><span class="sxs-lookup"><span data-stu-id="18dd5-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="18dd5-106">Tiene los privilegios mínimos en el equipo local y actúa como el equipo de la red.</span><span class="sxs-lookup"><span data-stu-id="18dd5-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="18dd5-107">Esta cuenta puede especificarse en una llamada a las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="18dd5-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="18dd5-108">Tenga en cuenta que esta cuenta no tiene contraseña, por lo que se omite cualquier información de contraseña que proporcione en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="18dd5-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="18dd5-109">Aunque el subsistema de seguridad localiza este nombre de cuenta, el SCM no admite nombres localizados.</span><span class="sxs-lookup"><span data-stu-id="18dd5-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="18dd5-110">Por lo tanto, recibirá un nombre traducido para esta cuenta desde la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , pero el nombre de la cuenta debe ser NT Authority \\ NetworkService cuando llame a **CreateService** o **ChangeServiceConfig**, independientemente de la configuración regional, o se puedan producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="18dd5-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="18dd5-111">Un servicio que se ejecuta en el contexto de la cuenta NetworkService presenta las credenciales del equipo a los servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="18dd5-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="18dd5-112">De forma predeterminada, el token remoto contiene los SID para los grupos todos y usuarios autenticados.</span><span class="sxs-lookup"><span data-stu-id="18dd5-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="18dd5-113">El SID de usuario se crea a partir del valor de **RID del servicio de red de seguridad \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="18dd5-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="18dd5-114">La cuenta NetworkService tiene su propia subclave en la clave del registro **HKEY \_ users** .</span><span class="sxs-lookup"><span data-stu-id="18dd5-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="18dd5-115">Por lo tanto, la clave del registro del **\_ \_ usuario actual HKEY** está asociada a la cuenta NetworkService.</span><span class="sxs-lookup"><span data-stu-id="18dd5-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="18dd5-116">La cuenta NetworkService tiene los siguientes privilegios:</span><span class="sxs-lookup"><span data-stu-id="18dd5-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="18dd5-117">**Se \_ \_Nombre de ASSIGNPRIMARYTOKEN** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="18dd5-118">**Se \_ \_Nombre de auditoría** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="18dd5-119">**Se \_ CAMBIAR \_ \_ el nombre** de la notificación (habilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="18dd5-120">**Se \_ CREAR \_ \_ nombre global** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="18dd5-121">**Se \_ \_Nombre de SUplantación** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="18dd5-122">**Se \_ AUMENTAR \_ \_ el nombre** de la cuota (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="18dd5-123">**Se \_ \_Nombre de apagado** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="18dd5-124">**Se \_ \_Nombre de desacoplamiento** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="18dd5-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="18dd5-125">Cualquier privilegio asignado a usuarios y usuarios autenticados</span><span class="sxs-lookup"><span data-stu-id="18dd5-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="18dd5-126">Para obtener más información, consulte [seguridad del servicio y derechos de acceso](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="18dd5-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
