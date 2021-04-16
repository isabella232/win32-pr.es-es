---
description: La cuenta LocalService es una cuenta local predefinida utilizada por el administrador de control de servicios.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Cuenta LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546515"
---
# <a name="localservice-account"></a><span data-ttu-id="9ddad-103">Cuenta LocalService</span><span class="sxs-lookup"><span data-stu-id="9ddad-103">LocalService Account</span></span>

<span data-ttu-id="9ddad-104">La cuenta LocalService es una cuenta local predefinida utilizada por el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="9ddad-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="9ddad-105">Tiene privilegios mínimos en el equipo local y presenta credenciales anónimas en la red.</span><span class="sxs-lookup"><span data-stu-id="9ddad-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="9ddad-106">Esta cuenta puede especificarse en una llamada a las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="9ddad-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="9ddad-107">Tenga en cuenta que esta cuenta no tiene contraseña, por lo que se omite cualquier información de contraseña que proporcione en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="9ddad-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="9ddad-108">Aunque el subsistema de seguridad localiza este nombre de cuenta, el SCM no admite nombres localizados.</span><span class="sxs-lookup"><span data-stu-id="9ddad-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="9ddad-109">Por lo tanto, recibirá un nombre traducido para esta cuenta desde la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , pero el nombre de la cuenta debe ser NT Authority \\ LocalService cuando llame a **CreateService** o **ChangeServiceConfig**, independientemente de la configuración regional, o se puedan producir resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="9ddad-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="9ddad-110">El SID de usuario se crea a partir del valor de **\_ \_ \_ RID del servicio local de seguridad** .</span><span class="sxs-lookup"><span data-stu-id="9ddad-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="9ddad-111">La cuenta LocalService tiene su propia subclave en la clave del registro **HKEY \_ users** .</span><span class="sxs-lookup"><span data-stu-id="9ddad-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="9ddad-112">Por lo tanto, la clave del registro del **\_ \_ usuario actual HKEY** está asociada a la cuenta LocalService.</span><span class="sxs-lookup"><span data-stu-id="9ddad-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="9ddad-113">La cuenta LocalService tiene los siguientes privilegios:</span><span class="sxs-lookup"><span data-stu-id="9ddad-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="9ddad-114">**Se \_ \_Nombre de ASSIGNPRIMARYTOKEN** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9ddad-115">**Se \_ \_Nombre de auditoría** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9ddad-116">**Se \_ CAMBIAR \_ \_ el nombre** de la notificación (habilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="9ddad-117">**Se \_ CREAR \_ \_ nombre global** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="9ddad-118">**Se \_ \_Nombre de SUplantación** (habilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="9ddad-119">**Se \_ AUMENTAR \_ \_ el nombre** de la cuota (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9ddad-120">**Se \_ \_Nombre de apagado** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9ddad-121">**Se \_ \_Nombre de desacoplamiento** (deshabilitado)</span><span class="sxs-lookup"><span data-stu-id="9ddad-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="9ddad-122">Cualquier privilegio asignado a usuarios y usuarios autenticados</span><span class="sxs-lookup"><span data-stu-id="9ddad-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="9ddad-123">Para obtener más información, consulte [seguridad del servicio y derechos de acceso](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="9ddad-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
