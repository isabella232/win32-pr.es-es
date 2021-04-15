---
description: La definición de la interfaz ISCardAuth se proporciona como un estándar que se puede seguir al desarrollar un proveedor de servicios de tarjetas inteligentes. La interfaz ISCardAuth se puede usar para exponer los servicios de autenticación admitidos por una tarjeta inteligente.
ms.assetid: 6b8a5b90-49ad-48fd-813c-c3c3337ec8f1
title: Interfaz ISCardAuth
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: bf8df3702aceb2ac8bbf5ad090802be2dc07e45a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497296"
---
# <a name="iscardauth-interface"></a><span data-ttu-id="798d9-103">Interfaz ISCardAuth</span><span class="sxs-lookup"><span data-stu-id="798d9-103">ISCardAuth interface</span></span>

<span data-ttu-id="798d9-104">\[La interfaz **ISCardAuth** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="798d9-104">\[The **ISCardAuth** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="798d9-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="798d9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="798d9-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="798d9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="798d9-107">La definición de la interfaz **ISCardAuth** se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios*](../secgloss/c-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="798d9-107">The **ISCardAuth** interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span>

<span data-ttu-id="798d9-108">La interfaz **ISCardAuth** se puede usar para exponer los servicios de autenticación admitidos por una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="798d9-108">The **ISCardAuth** interface can be used to expose authentication services supported by a smart card.</span></span> <span data-ttu-id="798d9-109">Estos servicios incluyen la autenticación de la aplicación, la autenticación mediante tarjeta inteligente y la autenticación de usuario.</span><span class="sxs-lookup"><span data-stu-id="798d9-109">These services include application authentication, smart card authentication, and user authentication.</span></span>

<span data-ttu-id="798d9-110">En el ejemplo siguiente se muestra un uso típico de la interfaz **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="798d9-110">The following example shows a typical use of the **ISCardAuth** interface.</span></span>

<span data-ttu-id="798d9-111">**Para usar ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="798d9-111">**To use ISCardAuth**</span></span>

1.  <span data-ttu-id="798d9-112">Cree una interfaz **ISCardAuth** (mediante el método de interfaz [**ISCardManage**](iscardmanage.md) correspondiente).</span><span class="sxs-lookup"><span data-stu-id="798d9-112">Create an **ISCardAuth** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="798d9-113">Llame al método **ISCardAuth** adecuado ([**\_ autenticación**](iscardauth-app-auth.md)de la aplicación, [**GetChallenge**](iscardauth-getchallenge.md), [**\_ autenticación ICC**](iscardauth-icc-auth.md)o [**\_ autenticación de usuario**](iscardauth-user-auth.md)).</span><span class="sxs-lookup"><span data-stu-id="798d9-113">Call the appropriate **ISCardAuth** method ([**APP\_Auth**](iscardauth-app-auth.md), [**GetChallenge**](iscardauth-getchallenge.md), [**ICC\_Auth**](iscardauth-icc-auth.md), or [**User\_Auth**](iscardauth-user-auth.md)).</span></span>
3.  <span data-ttu-id="798d9-114">Libere la interfaz **ISCardAuth** .</span><span class="sxs-lookup"><span data-stu-id="798d9-114">Release the **ISCardAuth** interface.</span></span>

## <a name="members"></a><span data-ttu-id="798d9-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="798d9-115">Members</span></span>

<span data-ttu-id="798d9-116">La interfaz **ISCardAuth** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="798d9-116">The **ISCardAuth** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="798d9-117">**ISCardAuth** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="798d9-117">**ISCardAuth** also has these types of members:</span></span>

-   [<span data-ttu-id="798d9-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="798d9-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="798d9-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="798d9-119">Methods</span></span>

<span data-ttu-id="798d9-120">La interfaz **ISCardAuth** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="798d9-120">The **ISCardAuth** interface has these methods.</span></span>



| <span data-ttu-id="798d9-121">Método</span><span class="sxs-lookup"><span data-stu-id="798d9-121">Method</span></span>                                          | <span data-ttu-id="798d9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="798d9-122">Description</span></span>                                                                                    |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="798d9-123">**Autenticación de la aplicación \_**</span><span class="sxs-lookup"><span data-stu-id="798d9-123">**APP\_Auth**</span></span>](iscardauth-app-auth.md)        | <span data-ttu-id="798d9-124">Permite que la aplicación se autentique mediante un protocolo de desafío/firma.</span><span class="sxs-lookup"><span data-stu-id="798d9-124">Allows the application to authenticate itself using a challenge/signature protocol.</span></span><br/> |
| [<span data-ttu-id="798d9-125">**GetChallenge**</span><span class="sxs-lookup"><span data-stu-id="798d9-125">**GetChallenge**</span></span>](iscardauth-getchallenge.md) | <span data-ttu-id="798d9-126">Devuelve un desafío de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="798d9-126">Returns a challenge from the smart card.</span></span><br/>                                            |
| [<span data-ttu-id="798d9-127">**Autenticación de ICC \_**</span><span class="sxs-lookup"><span data-stu-id="798d9-127">**ICC\_Auth**</span></span>](iscardauth-icc-auth.md)        | <span data-ttu-id="798d9-128">Permite que una aplicación autentique la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="798d9-128">Allows an application to authenticate the smart card.</span></span><br/>                               |
| [<span data-ttu-id="798d9-129">**Autenticación de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="798d9-129">**User\_Auth**</span></span>](iscardauth-user-auth.md)      | <span data-ttu-id="798d9-130">Permite el acceso a los servicios de autenticación de usuario.</span><span class="sxs-lookup"><span data-stu-id="798d9-130">Allows access to user authentication services.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="798d9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="798d9-131">Requirements</span></span>



| <span data-ttu-id="798d9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="798d9-132">Requirement</span></span> | <span data-ttu-id="798d9-133">Value</span><span class="sxs-lookup"><span data-stu-id="798d9-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="798d9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="798d9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="798d9-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="798d9-135">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="798d9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="798d9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="798d9-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="798d9-137">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="798d9-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="798d9-138">End of client support</span></span><br/>    | <span data-ttu-id="798d9-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="798d9-139">Windows XP</span></span><br/>                                |
| <span data-ttu-id="798d9-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="798d9-140">End of server support</span></span><br/>    | <span data-ttu-id="798d9-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="798d9-141">Windows Server 2003</span></span><br/>                       |



 

 
