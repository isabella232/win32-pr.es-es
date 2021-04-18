---
description: Interfaz implementada por el cliente que permite a los desarrolladores proporcionar sus propias credenciales de forma dinámica en tiempo de ejecución para autenticar los contenedores no Unidos a un dominio con Active Directory.
title: Interfaz ICcgDomainAuthCredentials (ccgplugins. h)
ms.topic: reference
ms.date: 10/20/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- ICcgDomainAuthCredentials
api_type:
- COM
api_location:
- ccgplugins.dll
ms.openlocfilehash: 8217f806ff0a1a6b38d045c7f665758ccaf8b1f5
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105721361"
---
# <a name="iccgdomainauthcredentials-interface"></a><span data-ttu-id="8066f-103">Interfaz ICcgDomainAuthCredentials</span><span class="sxs-lookup"><span data-stu-id="8066f-103">ICcgDomainAuthCredentials interface</span></span>

<span data-ttu-id="8066f-104">Interfaz implementada por el cliente que permite a los desarrolladores proporcionar sus propias credenciales de forma dinámica en tiempo de ejecución para autenticar los contenedores no Unidos a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8066f-104">A client-implemented interface that allows developers to supply their own credentials dynamically at run time to authenticate non-domain joined containers with Active Directory.</span></span> 

## <a name="members"></a><span data-ttu-id="8066f-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="8066f-105">Members</span></span>

<span data-ttu-id="8066f-106">La interfaz **ICcgDomainAuthCredentials** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8066f-106">The **ICcgDomainAuthCredentials** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8066f-107">**ICcgDomainAuthCredentials** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8066f-107">**ICcgDomainAuthCredentials** also has these types of members:</span></span>

-   [<span data-ttu-id="8066f-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8066f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8066f-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8066f-109">Methods</span></span>

<span data-ttu-id="8066f-110">La interfaz **ICcgDomainAuthCredentials** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8066f-110">The **ICcgDomainAuthCredentials** interface has these methods.</span></span>



| <span data-ttu-id="8066f-111">Método</span><span class="sxs-lookup"><span data-stu-id="8066f-111">Method</span></span>                                           | <span data-ttu-id="8066f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8066f-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8066f-113">**GetPasswordCredentials**</span><span class="sxs-lookup"><span data-stu-id="8066f-113">**GetPasswordCredentials**</span></span>](iccgdomainauthcredentials-getpasswordcredentials.md)               | <span data-ttu-id="8066f-114">Devuelve las credenciales para autenticar un contenedor no unido a un dominio con Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8066f-114">Returns credentials to authenticate a non-domain joined container with Active Directory.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="8066f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8066f-115">Requirements</span></span>



| <span data-ttu-id="8066f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8066f-116">Requirement</span></span> | <span data-ttu-id="8066f-117">Value</span><span class="sxs-lookup"><span data-stu-id="8066f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8066f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8066f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8066f-119">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="8066f-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8066f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8066f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8066f-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="8066f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8066f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8066f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8066f-123"><dt>ccgplugins. h</dt></span><span class="sxs-lookup"><span data-stu-id="8066f-123"><dt>ccgplugins.h</dt></span></span> </dl>   |
| <span data-ttu-id="8066f-124">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8066f-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="8066f-125"><dt>ccgplugins. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8066f-125"><dt>ccgplugins.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8066f-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8066f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8066f-127"><dt>ccgplugins.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8066f-127"><dt>ccgplugins.dll</dt></span></span> </dl> |
| <span data-ttu-id="8066f-128">IID</span><span class="sxs-lookup"><span data-stu-id="8066f-128">IID</span></span><br/>                      | <span data-ttu-id="8066f-129">6ecda518-2010-4437-8bc3-46e752b7b172</span><span class="sxs-lookup"><span data-stu-id="8066f-129">6ecda518-2010-4437-8bc3-46e752b7b172</span></span><br/>          |



 

