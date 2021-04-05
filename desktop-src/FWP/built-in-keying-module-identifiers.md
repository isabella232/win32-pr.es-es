---
title: Identificadores integrados del módulo de creación de claves (Fwpmu. h)
description: Los identificadores de los módulos de creación de claves integrados en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.
ms.assetid: ba3aaf0f-5524-4d61-bb74-e4714b11b2a9
topic_type:
- apiref
api_name:
- FWPM_KEYING_MODULE_IKE
- FWPM_KEYING_MODULE_IKEV2
- FWPM_KEYING_MODULE_AUTHIP
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9e6feb726a62de02130d64cef27cd9078395b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997061"
---
# <a name="built-in-keying-module-identifiers"></a><span data-ttu-id="0c6e7-103">Identificadores de módulo de incrustación integrados</span><span class="sxs-lookup"><span data-stu-id="0c6e7-103">Built-in Keying Module Identifiers</span></span>

<span data-ttu-id="0c6e7-104">Los identificadores de los módulos de creación de claves integrados en la plataforma de filtrado de Windows (WFP) se representan mediante un GUID.</span><span class="sxs-lookup"><span data-stu-id="0c6e7-104">The identifiers for the keying modules that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="0c6e7-105">Estos identificadores se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="0c6e7-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="0c6e7-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**\_módulo de generación de claves FWPM \_ \_ IKE**</span><span class="sxs-lookup"><span data-stu-id="0c6e7-106"><span id="FWPM_KEYING_MODULE_IKE"></span><span id="fwpm_keying_module_ike"></span>**FWPM\_KEYING\_MODULE\_IKE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c6e7-107">Módulo de creación de claves de Intercambio de claves por red (IKE).</span><span class="sxs-lookup"><span data-stu-id="0c6e7-107">Internet Key Exchange (IKE) keying module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c6e7-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**\_Módulo de generación de claves FWPM \_ \_ IKEV2**</span><span class="sxs-lookup"><span data-stu-id="0c6e7-108"><span id="FWPM_KEYING_MODULE_IKEV2"></span><span id="fwpm_keying_module_ikev2"></span>**FWPM\_KEYING\_MODULE\_IKEV2**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c6e7-109">Módulo de creación de claves de Intercambio de claves por red versión 2 (IKEv2).</span><span class="sxs-lookup"><span data-stu-id="0c6e7-109">Internet Key Exchange version 2 (IKEv2) keying module.</span></span>

> [!Note]  
> <span data-ttu-id="0c6e7-110">Solo está disponible en Windows Server 2008 R2 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0c6e7-110">Available only on Windows Server 2008 R2 and Windows 7.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="0c6e7-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**\_módulo de generación de claves FWPM \_ \_ AUTHIP**</span><span class="sxs-lookup"><span data-stu-id="0c6e7-111"><span id="FWPM_KEYING_MODULE_AUTHIP"></span><span id="fwpm_keying_module_authip"></span>**FWPM\_KEYING\_MODULE\_AUTHIP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0c6e7-112">Módulo de creación de claves de AuthIP.</span><span class="sxs-lookup"><span data-stu-id="0c6e7-112">AuthIP keying module.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c6e7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c6e7-113">Requirements</span></span>



| <span data-ttu-id="0c6e7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c6e7-114">Requirement</span></span> | <span data-ttu-id="0c6e7-115">Value</span><span class="sxs-lookup"><span data-stu-id="0c6e7-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6e7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c6e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0c6e7-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0c6e7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0c6e7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c6e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0c6e7-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c6e7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0c6e7-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c6e7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c6e7-121"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c6e7-121"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





