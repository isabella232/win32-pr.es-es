---
description: Proporciona servicios para establecer el código CHV (comprobación del titular de la tarjeta) y para comprobar el usuario.
ms.assetid: fa40c21c-1584-475e-89f6-f81f67e3b942
title: Interfaz ISCardVerify
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify
api_type:
- COM
api_location: ''
ms.openlocfilehash: f929028f96faaab6ddb03538e854db01196ae180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814379"
---
# <a name="iscardverify-interface"></a><span data-ttu-id="d3d23-103">Interfaz ISCardVerify</span><span class="sxs-lookup"><span data-stu-id="d3d23-103">ISCardVerify interface</span></span>

<span data-ttu-id="d3d23-104">\[La interfaz **ISCardVerify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="d3d23-104">\[The **ISCardVerify** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d3d23-105">No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d3d23-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d3d23-106">Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="d3d23-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="d3d23-107">La siguiente definición de interfaz se proporciona como un estándar que se puede seguir al desarrollar un [*proveedor de servicios*](../secgloss/c-gly.md)de [*tarjetas inteligentes*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="d3d23-107">The following interface definition is provided as a standard that can be followed when developing a [*smart card*](../secgloss/s-gly.md) [*service provider*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="d3d23-108">La interfaz **ISCardVerify** proporciona servicios para establecer el código CHV (comprobación del titular de la tarjeta) y para comprobar el usuario.</span><span class="sxs-lookup"><span data-stu-id="d3d23-108">The **ISCardVerify** interface provides services for setting CHV (card holder verification) code and for verifying the user.</span></span>

<span data-ttu-id="d3d23-109">La clase **ISCardVerify** se define para las aplicaciones que implementan la Directiva CHV específica de la aplicación y que tienen un conocimiento detallado de la implementación interna de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="d3d23-109">The **ISCardVerify** class is defined for applications that implement application-specific CHV policy, and that have a detailed knowledge of the smart card's internal implementation.</span></span>

<span data-ttu-id="d3d23-110">A continuación se usa el uso típico de la interfaz **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="d3d23-110">Following is a typical use of the **ISCardVerify** interface.</span></span>

<span data-ttu-id="d3d23-111">En el procedimiento siguiente se usa **ISCardVerify** para cambiar el código CHV.</span><span class="sxs-lookup"><span data-stu-id="d3d23-111">The following procedure uses **ISCardVerify** to change the CHV code.</span></span>

<span data-ttu-id="d3d23-112">**Para cambiar el código CHV de una tarjeta inteligente**</span><span class="sxs-lookup"><span data-stu-id="d3d23-112">**To change the CHV code of a smart card**</span></span>

1.  <span data-ttu-id="d3d23-113">Cree una interfaz **ISCardVerify** (mediante el método de interfaz [**ISCardManage**](iscardmanage.md) correspondiente).</span><span class="sxs-lookup"><span data-stu-id="d3d23-113">Create an **ISCardVerify** interface (through the corresponding [**ISCardManage**](iscardmanage.md) interface method).</span></span>
2.  <span data-ttu-id="d3d23-114">Llame al método [**ChangeCode**](iscardverify-changecode.md) y proporcione código nuevo, especificando si es local o global y si está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d3d23-114">Call the [**ChangeCode**](iscardverify-changecode.md) method and provide new code, specifying if it is local or global and if it is enabled or disabled.</span></span>
3.  <span data-ttu-id="d3d23-115">Libere la interfaz **ISCardVerify** .</span><span class="sxs-lookup"><span data-stu-id="d3d23-115">Release the **ISCardVerify** interface.</span></span>

## <a name="members"></a><span data-ttu-id="d3d23-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="d3d23-116">Members</span></span>

<span data-ttu-id="d3d23-117">La interfaz **ISCardVerify** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="d3d23-117">The **ISCardVerify** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="d3d23-118">**ISCardVerify** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d3d23-118">**ISCardVerify** also has these types of members:</span></span>

-   [<span data-ttu-id="d3d23-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3d23-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3d23-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="d3d23-120">Methods</span></span>

<span data-ttu-id="d3d23-121">La interfaz **ISCardVerify** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="d3d23-121">The **ISCardVerify** interface has these methods.</span></span>



| <span data-ttu-id="d3d23-122">Método</span><span class="sxs-lookup"><span data-stu-id="d3d23-122">Method</span></span>                                                        | <span data-ttu-id="d3d23-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3d23-123">Description</span></span>                                                                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3d23-124">**ChangeCode**</span><span class="sxs-lookup"><span data-stu-id="d3d23-124">**ChangeCode**</span></span>](iscardverify-changecode.md)                 | <span data-ttu-id="d3d23-125">Cambia el código CHV actual.</span><span class="sxs-lookup"><span data-stu-id="d3d23-125">Changes the current CHV code.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="d3d23-126">**ResetSecurityState**</span><span class="sxs-lookup"><span data-stu-id="d3d23-126">**ResetSecurityState**</span></span>](iscardverify-resetsecuritystate.md) | <span data-ttu-id="d3d23-127">Restablece el [*contexto de seguridad*](../secgloss/s-gly.md) de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="d3d23-127">Resets the [*security context*](../secgloss/s-gly.md) of the smart card.</span></span><br/> |
| <span data-ttu-id="d3d23-128">[**Desbloquear**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d3d23-128">[**Unblock**](/previous-versions/windows/desktop/legacy/aa377269(v=vs.85))</span></span>                       | <span data-ttu-id="d3d23-129">Vuelve a habilitar el [*contexto de seguridad*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="d3d23-129">Re-enables the [*security context*](../secgloss/s-gly.md).</span></span><br/>               |
| [<span data-ttu-id="d3d23-130">**Ver**</span><span class="sxs-lookup"><span data-stu-id="d3d23-130">**Verify**</span></span>](iscardverify-verify.md)                         | <span data-ttu-id="d3d23-131">Autentica al usuario.</span><span class="sxs-lookup"><span data-stu-id="d3d23-131">Authenticates the user.</span></span><br/>                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="d3d23-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3d23-132">Requirements</span></span>



| <span data-ttu-id="d3d23-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3d23-133">Requirement</span></span> | <span data-ttu-id="d3d23-134">Value</span><span class="sxs-lookup"><span data-stu-id="d3d23-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d3d23-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3d23-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d3d23-136">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d3d23-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="d3d23-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3d23-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d3d23-138">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3d23-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d3d23-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="d3d23-139">End of client support</span></span><br/>    | <span data-ttu-id="d3d23-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="d3d23-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="d3d23-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="d3d23-141">End of server support</span></span><br/>    | <span data-ttu-id="d3d23-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d3d23-142">Windows Server 2003</span></span><br/>                       |



 

 
