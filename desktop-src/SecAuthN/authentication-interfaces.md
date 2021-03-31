---
description: Enumera las interfaces de las API de autenticación.
ms.assetid: bde3bcae-2152-4589-92a0-b44d98f233ef
title: Interfaces de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b101fd4fdd3c518d24b5b6f798fcaa4e0327dd22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277350"
---
# <a name="authentication-interfaces"></a><span data-ttu-id="e1bb4-103">Interfaces de autenticación</span><span class="sxs-lookup"><span data-stu-id="e1bb4-103">Authentication Interfaces</span></span>

<span data-ttu-id="e1bb4-104">Las interfaces de autenticación se clasifican según el uso de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="e1bb4-104">Authentication interfaces are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="e1bb4-105">Interfaces de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e1bb4-105">Smart Card Interfaces</span></span>](#smart-card-interfaces)
-   [<span data-ttu-id="e1bb4-106">Interfaces de uso compartido de identidad</span><span class="sxs-lookup"><span data-stu-id="e1bb4-106">Identity Sharing Interfaces</span></span>](#identity-sharing-interfaces)

## <a name="smart-card-interfaces"></a><span data-ttu-id="e1bb4-107">Interfaces de tarjeta inteligente</span><span class="sxs-lookup"><span data-stu-id="e1bb4-107">Smart Card Interfaces</span></span>

<span data-ttu-id="e1bb4-108">El SDK de tarjeta inteligente proporciona las siguientes interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-108">The Smart Card SDK provides the following COM interfaces.</span></span> <span data-ttu-id="e1bb4-109">Los métodos para una interfaz específica se enumeran en la tabla de contenido y en la página de referencia de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-109">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="e1bb4-110">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e1bb4-110">Interface</span></span>                                    | <span data-ttu-id="e1bb4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1bb4-111">Description</span></span>                                                                                                                                                                              |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1bb4-112">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-112">**IByteBuffer**</span></span>](ibytebuffer.md)           | <span data-ttu-id="e1bb4-113">Administra un objeto de flujo.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-113">Manages a stream object.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="e1bb4-114">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-114">**ISCard**</span></span>](iscard.md)                     | <span data-ttu-id="e1bb4-115">Abre y administra una conexión a una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="e1bb4-115">Opens and manages a connection to a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span>                                                                    |
| [<span data-ttu-id="e1bb4-116">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-116">**ISCardAuth**</span></span>](iscardauth.md)             | <span data-ttu-id="e1bb4-117">Autentica una aplicación, una tarjeta inteligente o un usuario.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-117">Authenticates an application, smart card, or user.</span></span>                                                                                                                                       |
| [<span data-ttu-id="e1bb4-118">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-118">**ISCardCmd**</span></span>](iscardcmd.md)               | <span data-ttu-id="e1bb4-119">Construye y administra una [*unidad de datos de protocolo de aplicación*](/windows/desktop/SecGloss/a-gly) de tarjeta inteligente (APDU).</span><span class="sxs-lookup"><span data-stu-id="e1bb4-119">Constructs and manages a smart card [*Application Protocol Data Unit*](/windows/desktop/SecGloss/a-gly) (APDU).</span></span> |
| [<span data-ttu-id="e1bb4-120">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-120">**ISCardDatabase**</span></span>](iscarddatabase.md)     | <span data-ttu-id="e1bb4-121">Realiza operaciones de base de datos del [*Administrador de recursos*](/windows/desktop/SecGloss/r-gly) de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-121">Performs smart card [*resource manager*](/windows/desktop/SecGloss/r-gly) database operations.</span></span>                                              |
| [<span data-ttu-id="e1bb4-122">**ISCardFileAccess**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-122">**ISCardFileAccess**</span></span>](iscardfileaccess.md) | <span data-ttu-id="e1bb4-123">Realiza servicios de archivo comunes, como buscar, seleccionar, leer, escribir, crear y eliminar archivos.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-123">Performs common file services such as locating, selecting, reading, writing, creating, and deleting files.</span></span>                                                                               |
| [<span data-ttu-id="e1bb4-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-124">**ISCardISO7816**</span></span>](iscardiso7816.md)       | <span data-ttu-id="e1bb4-125">Construye un comando APDU.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-125">Constructs an APDU command.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="e1bb4-126">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-126">**ISCardLocate**</span></span>](iscardlocate.md)         | <span data-ttu-id="e1bb4-127">Busca una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-127">Locates a smart card.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="e1bb4-128">**ISCardManage**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-128">**ISCardManage**</span></span>](iscardmanage.md)         | <span data-ttu-id="e1bb4-129">Administra el sistema de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-129">Manages the smart card system.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="e1bb4-130">**ISCardTypeConv**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-130">**ISCardTypeConv**</span></span>](iscardtypeconv.md)     | <span data-ttu-id="e1bb4-131">Proporciona métodos que se usan para admitir otras interfaces COM de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-131">Provides methods used to support other smart card COM interfaces.</span></span> <span data-ttu-id="e1bb4-132">Esta interfaz se proporciona solo para la compatibilidad con versiones anteriores y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-132">This interface is provided for backward compatibility only and should no longer be used.</span></span>                               |
| [<span data-ttu-id="e1bb4-133">**ISCardVerify**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-133">**ISCardVerify**</span></span>](iscardverify.md)         | <span data-ttu-id="e1bb4-134">Comprueba o cambia la Directiva de comprobación del titular de la tarjeta (CHV).</span><span class="sxs-lookup"><span data-stu-id="e1bb4-134">Verifies or changes card holder verification (CHV) policy.</span></span>                                                                                                                               |



 

## <a name="identity-sharing-interfaces"></a><span data-ttu-id="e1bb4-135">Interfaces de uso compartido de identidad</span><span class="sxs-lookup"><span data-stu-id="e1bb4-135">Identity Sharing Interfaces</span></span>

<span data-ttu-id="e1bb4-136">El SDK de uso compartido de identidades proporciona las siguientes interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-136">The Identity Sharing SDK provides the following COM interfaces.</span></span> <span data-ttu-id="e1bb4-137">Los métodos para una interfaz específica se enumeran en la tabla de contenido y en la página de referencia de esa interfaz.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-137">The methods for a specific interface are listed in the Table of Contents and on the reference page for that interface.</span></span>



| <span data-ttu-id="e1bb4-138">Interfaz</span><span class="sxs-lookup"><span data-stu-id="e1bb4-138">Interface</span></span>                                                          | <span data-ttu-id="e1bb4-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1bb4-139">Description</span></span>                                                                              |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e1bb4-140">**IAssociatedIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-140">**IAssociatedIdentityProvider**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iassociatedidentityprovider) | <span data-ttu-id="e1bb4-141">Permite a un proveedor de identidades asociar identidades con cuentas de usuario locales.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-141">Allows an identity provider to associate identities with local user accounts.</span></span>            |
| [<span data-ttu-id="e1bb4-142">**IIdentityAdvise**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-142">**IIdentityAdvise**</span></span>](/windows/desktop/api/IdentityProvider/nn-identityprovider-iidentityadvise)                         | <span data-ttu-id="e1bb4-143">Permite a un proveedor de identidades notificar a una aplicación que realiza la llamada cuando se actualiza una identidad.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-143">Allows an identity provider to notify a calling application when an identity is updated.</span></span> |
| [<span data-ttu-id="e1bb4-144">**IIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-144">**IIdentityProvider**</span></span>](/windows/desktop/api/Identityprovider/nn-identityprovider-iidentityprovider)                     | <span data-ttu-id="e1bb4-145">Representa un proveedor de identidad.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-145">Represents an identity provider.</span></span>                                                         |
| [<span data-ttu-id="e1bb4-146">**IIdentityStore**</span><span class="sxs-lookup"><span data-stu-id="e1bb4-146">**IIdentityStore**</span></span>](/windows/desktop/api/Identitystore/nn-identitystore-iidentitystore)                           | <span data-ttu-id="e1bb4-147">Proporciona métodos para enumerar y administrar identidades y proveedores de identidades.</span><span class="sxs-lookup"><span data-stu-id="e1bb4-147">Provides methods to enumerate and manage identities and identity providers.</span></span>              |



 

 

 
