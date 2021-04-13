---
title: atributo MS-TPM-SRK-pub-Thumbprint
description: Este atributo contiene la huella digital del SrkPub correspondiente a un determinado TPM. Esto ayuda a indexar los dispositivos de TPM en el directorio.
ms.assetid: 64cb0341-ae49-4992-87d7-6863719fa13f
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-TPM-SRK-pub-Thumbprint
- msTPM-SrkPubThumbprint atributo AD Schema
topic_type:
- apiref
api_name:
- ms-TPM-Srk-Pub-Thumbprint
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf2ab2daec38d509e670771eef61824278bee4c4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104536208"
---
# <a name="ms-tpm-srk-pub-thumbprint-attribute"></a><span data-ttu-id="74539-106">atributo MS-TPM-SRK-pub-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="74539-106">ms-TPM-Srk-Pub-Thumbprint attribute</span></span>

<span data-ttu-id="74539-107">Este atributo contiene la huella digital del SrkPub correspondiente a un determinado TPM.</span><span class="sxs-lookup"><span data-stu-id="74539-107">This attribute contains the thumbprint of the SrkPub corresponding to a particular TPM.</span></span> <span data-ttu-id="74539-108">Esto ayuda a indexar los dispositivos de TPM en el directorio.</span><span class="sxs-lookup"><span data-stu-id="74539-108">This helps to index the TPM devices in the directory.</span></span>



| <span data-ttu-id="74539-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="74539-109">Entry</span></span> | <span data-ttu-id="74539-110">Value</span><span class="sxs-lookup"><span data-stu-id="74539-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="74539-111">CN</span><span class="sxs-lookup"><span data-stu-id="74539-111">CN</span></span>                | <span data-ttu-id="74539-112">MS-TPM-SRK-pub-huella digital</span><span class="sxs-lookup"><span data-stu-id="74539-112">ms-TPM-Srk-Pub-Thumbprint</span></span>                             |
| <span data-ttu-id="74539-113">Nombre para mostrar de LDAP</span><span class="sxs-lookup"><span data-stu-id="74539-113">Ldap-Display-Name</span></span> | <span data-ttu-id="74539-114">msTPM-SrkPubThumbprint</span><span class="sxs-lookup"><span data-stu-id="74539-114">msTPM-SrkPubThumbprint</span></span>                                |
| <span data-ttu-id="74539-115">Tamaño</span><span class="sxs-lookup"><span data-stu-id="74539-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="74539-116">Actualizar privilegio</span><span class="sxs-lookup"><span data-stu-id="74539-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="74539-117">Frecuencia de actualización</span><span class="sxs-lookup"><span data-stu-id="74539-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="74539-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="74539-118">Attribute-Id</span></span>      | <span data-ttu-id="74539-119">1.2.840.113556.1.4.2107</span><span class="sxs-lookup"><span data-stu-id="74539-119">1.2.840.113556.1.4.2107</span></span>                               |
| <span data-ttu-id="74539-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="74539-120">System-Id-Guid</span></span>    | <span data-ttu-id="74539-121">19d706eb-4d76-44a2-85d6-1c342be3be37</span><span class="sxs-lookup"><span data-stu-id="74539-121">19d706eb-4d76-44a2-85d6-1c342be3be37</span></span>                  |
| <span data-ttu-id="74539-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74539-122">Syntax</span></span>            | [<span data-ttu-id="74539-123">**Object(Replica-Link)**</span><span class="sxs-lookup"><span data-stu-id="74539-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="74539-124">Implementaciones</span><span class="sxs-lookup"><span data-stu-id="74539-124">Implementations</span></span>

-   [<span data-ttu-id="74539-125">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="74539-125">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2012"></a><span data-ttu-id="74539-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74539-126">Windows Server 2012</span></span>



| <span data-ttu-id="74539-127">Entrada</span><span class="sxs-lookup"><span data-stu-id="74539-127">Entry</span></span> | <span data-ttu-id="74539-128">Value</span><span class="sxs-lookup"><span data-stu-id="74539-128">Value</span></span> |
|------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="74539-129">Identificador de vínculo</span><span class="sxs-lookup"><span data-stu-id="74539-129">Link-Id</span></span>                | \-                                                                        |
| <span data-ttu-id="74539-130">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="74539-130">MAPI-Id</span></span>                | \-                                                                        |
| <span data-ttu-id="74539-131">System-Only</span><span class="sxs-lookup"><span data-stu-id="74539-131">System-Only</span></span>            | <span data-ttu-id="74539-132">False</span><span class="sxs-lookup"><span data-stu-id="74539-132">False</span></span>                                                                     |
| <span data-ttu-id="74539-133">Tiene un único valor</span><span class="sxs-lookup"><span data-stu-id="74539-133">Is-Single-Valued</span></span>       | <span data-ttu-id="74539-134">True</span><span class="sxs-lookup"><span data-stu-id="74539-134">True</span></span>                                                                      |
| <span data-ttu-id="74539-135">Está indexado</span><span class="sxs-lookup"><span data-stu-id="74539-135">Is Indexed</span></span>             | <span data-ttu-id="74539-136">True</span><span class="sxs-lookup"><span data-stu-id="74539-136">True</span></span>                                                                      |
| <span data-ttu-id="74539-137">En el catálogo global</span><span class="sxs-lookup"><span data-stu-id="74539-137">In Global Catalog</span></span>      | <span data-ttu-id="74539-138">False</span><span class="sxs-lookup"><span data-stu-id="74539-138">False</span></span>                                                                     |
| <span data-ttu-id="74539-139">Descriptor de NT-Security-</span><span class="sxs-lookup"><span data-stu-id="74539-139">NT-Security-Descriptor</span></span> | <span data-ttu-id="74539-140">O:BAG: BAD: S:</span><span class="sxs-lookup"><span data-stu-id="74539-140">O:BAG:BAD:S:</span></span>                                                              |
| <span data-ttu-id="74539-141">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="74539-141">Range-Lower</span></span>            | \-                                                                        |
| <span data-ttu-id="74539-142">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="74539-142">Range-Upper</span></span>            | \-                                                                        |
| <span data-ttu-id="74539-143">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="74539-143">Search-Flags</span></span>           | <span data-ttu-id="74539-144">0x0000000B</span><span class="sxs-lookup"><span data-stu-id="74539-144">0x0000000B</span></span>                                                                |
| <span data-ttu-id="74539-145">System-Flags</span><span class="sxs-lookup"><span data-stu-id="74539-145">System-Flags</span></span>           | <span data-ttu-id="74539-146">0x00000010</span><span class="sxs-lookup"><span data-stu-id="74539-146">0x00000010</span></span>                                                                |
| <span data-ttu-id="74539-147">Clases usadas en</span><span class="sxs-lookup"><span data-stu-id="74539-147">Classes used in</span></span>        | [<span data-ttu-id="74539-148">**Objeto de información de MS-TPM**</span><span class="sxs-lookup"><span data-stu-id="74539-148">**ms-TPM-Information-Object**</span></span>](c-mstpm-informationobject.md)<br/> |



 

 





