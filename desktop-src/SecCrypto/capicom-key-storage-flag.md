---
description: La enumeración de marcas de almacenamiento de claves de CAPICOM \_ \_ define las marcas de almacenamiento de \_ claves.
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Enumeración CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 9edbc3a5ac3396e528ebbb5390c4b07c24770e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649780"
---
# <a name="capicom_key_storage_flag-enumeration"></a><span data-ttu-id="0ad0f-103">\_ \_ Enumeración de marcas de almacenamiento de claves de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="0ad0f-103">CAPICOM\_KEY\_STORAGE\_FLAG enumeration</span></span>

<span data-ttu-id="0ad0f-104">La enumeración de marcas de almacenamiento de claves de CAPICOM define las marcas de almacenamiento de claves. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0ad0f-104">The **CAPICOM\_KEY\_STORAGE\_FLAG** enumeration defines key storage flags.</span></span>

## <a name="members"></a><span data-ttu-id="0ad0f-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="0ad0f-105">Members</span></span>



| <span data-ttu-id="0ad0f-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="0ad0f-106">Member</span></span>                                     | <span data-ttu-id="0ad0f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ad0f-107">Description</span></span>                           | <span data-ttu-id="0ad0f-108">Value</span><span class="sxs-lookup"><span data-stu-id="0ad0f-108">Value</span></span> |
|--------------------------------------------|---------------------------------------|-------|
| <span data-ttu-id="0ad0f-109">**CAPICOM \_ , \_ valor predeterminado de almacenamiento de claves \_**</span><span class="sxs-lookup"><span data-stu-id="0ad0f-109">**CAPICOM\_KEY\_STORAGE\_DEFAULT**</span></span>         | <span data-ttu-id="0ad0f-110">Almacenamiento de claves predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0ad0f-110">Default key storage.</span></span><br/>       | <span data-ttu-id="0ad0f-111">0</span><span class="sxs-lookup"><span data-stu-id="0ad0f-111">0</span></span>     |
| <span data-ttu-id="0ad0f-112">**el \_ almacenamiento de claves de CAPICOM \_ \_ exportable**</span><span class="sxs-lookup"><span data-stu-id="0ad0f-112">**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</span></span>      | <span data-ttu-id="0ad0f-113">La clave es exportable.</span><span class="sxs-lookup"><span data-stu-id="0ad0f-113">The key is exportable.</span></span><br/>     | <span data-ttu-id="0ad0f-114">1</span><span class="sxs-lookup"><span data-stu-id="0ad0f-114">1</span></span>     |
| <span data-ttu-id="0ad0f-115">**CAPICOM \_ \_ protección del \_ usuario de almacenamiento de claves \_**</span><span class="sxs-lookup"><span data-stu-id="0ad0f-115">**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</span></span> | <span data-ttu-id="0ad0f-116">La clave está protegida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="0ad0f-116">The key is user protected.</span></span><br/> | <span data-ttu-id="0ad0f-117">2</span><span class="sxs-lookup"><span data-stu-id="0ad0f-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="0ad0f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ad0f-118">Remarks</span></span>

<span data-ttu-id="0ad0f-119">Esta enumeración la usa el método siguiente:</span><span class="sxs-lookup"><span data-stu-id="0ad0f-119">This enumeration is used by the following method:</span></span>

-   [<span data-ttu-id="0ad0f-120">**Certificate. Load**</span><span class="sxs-lookup"><span data-stu-id="0ad0f-120">**Certificate.Load**</span></span>](certificate-load.md)
-   [<span data-ttu-id="0ad0f-121">**Store. Load**</span><span class="sxs-lookup"><span data-stu-id="0ad0f-121">**Store.Load**</span></span>](store-load.md)

## <a name="requirements"></a><span data-ttu-id="0ad0f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ad0f-122">Requirements</span></span>



| <span data-ttu-id="0ad0f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ad0f-123">Requirement</span></span> | <span data-ttu-id="0ad0f-124">Value</span><span class="sxs-lookup"><span data-stu-id="0ad0f-124">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad0f-125">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0ad0f-125">Redistributable</span></span><br/> | <span data-ttu-id="0ad0f-126">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ad0f-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0ad0f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ad0f-127">Header</span></span><br/>          | <dl> <span data-ttu-id="0ad0f-128"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ad0f-128"><dt>Capicom.h</dt></span></span> </dl> |



 

 




