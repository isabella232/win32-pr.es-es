---
description: Indica qué se comprueba cuando se comprueba una firma digital.
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: Enumeración CAPICOM_SIGNED_DATA_VERIFY_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671366"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="f62f4-103">\_ \_ \_ Enumeración de marca de comprobación de datos FIRMAdos de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="f62f4-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="f62f4-104">La enumeración de **\_ marcas de \_ \_ verificación \_ de datos firmados de CAPICOM** indica lo que se comprueba cuando se comprueba una [*firma digital*](../secgloss/d-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f62f4-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="f62f4-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="f62f4-105">Members</span></span>



| <span data-ttu-id="f62f4-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="f62f4-106">Member</span></span>                                           | <span data-ttu-id="f62f4-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f62f4-107">Description</span></span>                                                                                                 | <span data-ttu-id="f62f4-108">Value</span><span class="sxs-lookup"><span data-stu-id="f62f4-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="f62f4-109">**CAPICOM \_ comprobar \_ solo la firma \_**</span><span class="sxs-lookup"><span data-stu-id="f62f4-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="f62f4-110">Solo se comprueba la firma.</span><span class="sxs-lookup"><span data-stu-id="f62f4-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="f62f4-111">0</span><span class="sxs-lookup"><span data-stu-id="f62f4-111">0</span></span>     |
| <span data-ttu-id="f62f4-112">**CAPICOM \_ comprobar la \_ firma \_ y el \_ certificado**</span><span class="sxs-lookup"><span data-stu-id="f62f4-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="f62f4-113">Se comprueban tanto la firma como la validez del certificado utilizado para crear la firma.</span><span class="sxs-lookup"><span data-stu-id="f62f4-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="f62f4-114">1</span><span class="sxs-lookup"><span data-stu-id="f62f4-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="f62f4-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f62f4-115">Requirements</span></span>



| <span data-ttu-id="f62f4-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f62f4-116">Requirement</span></span> | <span data-ttu-id="f62f4-117">Value</span><span class="sxs-lookup"><span data-stu-id="f62f4-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f62f4-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f62f4-118">Redistributable</span></span><br/> | <span data-ttu-id="f62f4-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="f62f4-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="f62f4-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f62f4-120">Header</span></span><br/>          | <dl> <span data-ttu-id="f62f4-121"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f62f4-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
