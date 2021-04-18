---
description: Se utiliza con el método Store. Open para indicar cómo se va a abrir un almacén de certificados.
ms.assetid: 6ec87b8c-9431-4ecc-bd90-943cfe2df1c2
title: Enumeración CAPICOM_STORE_OPEN_MODE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_OPEN_MODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 61fe8be0bdf75db5204066563ca07f8225678f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650006"
---
# <a name="capicom_store_open_mode-enumeration"></a><span data-ttu-id="a66bb-103">\_ \_ Enumeración de modo de apertura de la tienda CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="a66bb-103">CAPICOM\_STORE\_OPEN\_MODE enumeration</span></span>

<span data-ttu-id="a66bb-104">El \_ tipo de \_ enumeración de modo abierto de CAPICOM \_ se utiliza con el método [**Store. Open**](store-open.md) para indicar cómo se va a abrir un almacén de certificados.</span><span class="sxs-lookup"><span data-stu-id="a66bb-104">The CAPICOM\_STORE\_OPEN\_MODE enumeration type is used with the [**Store.Open**](store-open.md) method to indicate how a certificate store is to be opened.</span></span>

## <a name="members"></a><span data-ttu-id="a66bb-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="a66bb-105">Members</span></span>



| <span data-ttu-id="a66bb-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="a66bb-106">Member</span></span>                                      | <span data-ttu-id="a66bb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a66bb-107">Description</span></span>                                                                                                                                                              | <span data-ttu-id="a66bb-108">Value</span><span class="sxs-lookup"><span data-stu-id="a66bb-108">Value</span></span> |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="a66bb-109">**CAPICOM \_ Store \_ Open \_ Read \_ Only**</span><span class="sxs-lookup"><span data-stu-id="a66bb-109">**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</span></span>        | <span data-ttu-id="a66bb-110">Abra el almacén en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a66bb-110">Open the store in read-only mode.</span></span><br/>                                                                                                                             | <span data-ttu-id="a66bb-111">0</span><span class="sxs-lookup"><span data-stu-id="a66bb-111">0</span></span>     |
| <span data-ttu-id="a66bb-112">**CAPICOM \_ Store \_ Open \_ Read \_ Write**</span><span class="sxs-lookup"><span data-stu-id="a66bb-112">**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</span></span>       | <span data-ttu-id="a66bb-113">Abra el almacén en modo de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a66bb-113">Open the store in read/write mode.</span></span><br/>                                                                                                                            | <span data-ttu-id="a66bb-114">1</span><span class="sxs-lookup"><span data-stu-id="a66bb-114">1</span></span>     |
| <span data-ttu-id="a66bb-115">**\_ \_ \_ máximo permitido del almacén \_ de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="a66bb-115">**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</span></span>  | <span data-ttu-id="a66bb-116">Abra el almacén en modo de lectura y escritura si el usuario tiene permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a66bb-116">Open the store in read/write mode if the user has read/write permissions.</span></span> <span data-ttu-id="a66bb-117">Si el usuario no tiene permisos de lectura/escritura, abra el almacén en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="a66bb-117">If the user does not have read/write permissions, open the store in read-only mode.</span></span><br/> | <span data-ttu-id="a66bb-118">2</span><span class="sxs-lookup"><span data-stu-id="a66bb-118">2</span></span>     |
| <span data-ttu-id="a66bb-119">**CAPICOM \_ Store \_ Open \_ exist \_ Only**</span><span class="sxs-lookup"><span data-stu-id="a66bb-119">**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</span></span>    | <span data-ttu-id="a66bb-120">Abrir solo los almacenes existentes; no cree un nuevo almacén.</span><span class="sxs-lookup"><span data-stu-id="a66bb-120">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="a66bb-121">Introducido por CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a66bb-121">Introduced by CAPICOM 2.0.</span></span><br/>                                                                              | <span data-ttu-id="a66bb-122">128</span><span class="sxs-lookup"><span data-stu-id="a66bb-122">128</span></span>   |
| <span data-ttu-id="a66bb-123">**\_ \_ archivos abiertos de \_ la tienda de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="a66bb-123">**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</span></span> | <span data-ttu-id="a66bb-124">Incluir certificados archivados al usar el almacén.</span><span class="sxs-lookup"><span data-stu-id="a66bb-124">Include archived certificates when using the store.</span></span> <span data-ttu-id="a66bb-125">Introducido por CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a66bb-125">Introduced by CAPICOM 2.0.</span></span><br/>                                                                                | <span data-ttu-id="a66bb-126">256</span><span class="sxs-lookup"><span data-stu-id="a66bb-126">256</span></span>   |



## <a name="remarks"></a><span data-ttu-id="a66bb-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a66bb-127">Remarks</span></span>

<span data-ttu-id="a66bb-128">Al utilizar la \_ \_ enumeración de modo abierto de la tienda CAPICOM \_ , solo se puede usar una de las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="a66bb-128">When using the CAPICOM\_STORE\_OPEN\_MODE enumeration, only one of the following settings can be used.</span></span>

-   <span data-ttu-id="a66bb-129">CAPICOM \_ Store \_ Open \_ Read \_ Only</span><span class="sxs-lookup"><span data-stu-id="a66bb-129">CAPICOM\_STORE\_OPEN\_READ\_ONLY</span></span>
-   <span data-ttu-id="a66bb-130">CAPICOM \_ Store \_ Open \_ Read \_ Write</span><span class="sxs-lookup"><span data-stu-id="a66bb-130">CAPICOM\_STORE\_OPEN\_READ\_WRITE</span></span>
-   <span data-ttu-id="a66bb-131">\_ \_ \_ máximo permitido del almacén \_ de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="a66bb-131">CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED</span></span>

## <a name="requirements"></a><span data-ttu-id="a66bb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a66bb-132">Requirements</span></span>



| <span data-ttu-id="a66bb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a66bb-133">Requirement</span></span> | <span data-ttu-id="a66bb-134">Value</span><span class="sxs-lookup"><span data-stu-id="a66bb-134">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a66bb-135">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a66bb-135">Redistributable</span></span><br/> | <span data-ttu-id="a66bb-136">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a66bb-136">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="a66bb-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a66bb-137">Header</span></span><br/>          | <dl> <span data-ttu-id="a66bb-138"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a66bb-138"><dt>Capicom.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a66bb-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a66bb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66bb-140">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="a66bb-140">**Store.Open**</span></span>](store-open.md)
</dt> </dl>

 

 




