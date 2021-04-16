---
description: Indica la ubicación de un almacén de certificados.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Enumeración CAPICOM_STORE_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671365"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="397b8-103">\_Enumeración de ubicación del almacén de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="397b8-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="397b8-104">El tipo de enumeración **\_ \_ Ubicación del almacén de CAPICOM** indica la ubicación de un almacén de [*certificados*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="397b8-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="397b8-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="397b8-105">Members</span></span>



| <span data-ttu-id="397b8-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="397b8-106">Member</span></span>                                      | <span data-ttu-id="397b8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="397b8-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="397b8-108">Value</span><span class="sxs-lookup"><span data-stu-id="397b8-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="397b8-109">**\_almacén de memoria CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="397b8-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="397b8-110">El almacén es un almacén de memoria.</span><span class="sxs-lookup"><span data-stu-id="397b8-110">The store is a memory store.</span></span> <span data-ttu-id="397b8-111">No se conservan los cambios en el contenido del almacén.</span><span class="sxs-lookup"><span data-stu-id="397b8-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="397b8-112">0</span><span class="sxs-lookup"><span data-stu-id="397b8-112">0</span></span>     |
| <span data-ttu-id="397b8-113">**\_almacén del \_ equipo \_ local de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="397b8-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="397b8-114">El almacén es un almacén del equipo local.</span><span class="sxs-lookup"><span data-stu-id="397b8-114">The store is a local machine store.</span></span> <span data-ttu-id="397b8-115">Los almacenes de máquinas locales pueden ser almacenes de lectura y escritura solo si el usuario tiene permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="397b8-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="397b8-116">Si el usuario tiene permisos de lectura y escritura y si el almacén está abierto para lectura y escritura, se conservan los cambios en el contenido del almacén.</span><span class="sxs-lookup"><span data-stu-id="397b8-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="397b8-117">1</span><span class="sxs-lookup"><span data-stu-id="397b8-117">1</span></span>     |
| <span data-ttu-id="397b8-118">**\_almacén de \_ usuarios \_ actual de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="397b8-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="397b8-119">El almacén es un almacén de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="397b8-119">The store is a current user store.</span></span> <span data-ttu-id="397b8-120">Un almacén de usuario actual puede ser un almacén de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="397b8-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="397b8-121">Si es así, se conservan los cambios en el contenido del almacén.</span><span class="sxs-lookup"><span data-stu-id="397b8-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="397b8-122">2</span><span class="sxs-lookup"><span data-stu-id="397b8-122">2</span></span>     |
| <span data-ttu-id="397b8-123">**el \_ \_ almacén de \_ usuarios de Active \_ Directory de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="397b8-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="397b8-124">El almacén es un almacén de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="397b8-124">The store is an Active Directory store.</span></span> <span data-ttu-id="397b8-125">Active Directory almacenes solo se pueden abrir en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="397b8-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="397b8-126">Los certificados no se pueden agregar ni quitar de Active Directory almacenes.</span><span class="sxs-lookup"><span data-stu-id="397b8-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="397b8-127">3</span><span class="sxs-lookup"><span data-stu-id="397b8-127">3</span></span>     |
| <span data-ttu-id="397b8-128">**el \_ \_ almacén de \_ usuarios de tarjetas inteligentes CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="397b8-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="397b8-129">Los almacenes admiten almacenes de certificados basados en tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="397b8-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="397b8-130">El almacén es el grupo de tarjetas inteligentes presentes.</span><span class="sxs-lookup"><span data-stu-id="397b8-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="397b8-131">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="397b8-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="397b8-132">4</span><span class="sxs-lookup"><span data-stu-id="397b8-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="397b8-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="397b8-133">Remarks</span></span>

<span data-ttu-id="397b8-134">Los métodos siguientes utilizan el tipo de enumeración de **\_ \_ Ubicación de almacén de CAPICOM** :</span><span class="sxs-lookup"><span data-stu-id="397b8-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="397b8-135">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="397b8-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="397b8-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="397b8-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="397b8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="397b8-137">Requirements</span></span>



| <span data-ttu-id="397b8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="397b8-138">Requirement</span></span> | <span data-ttu-id="397b8-139">Value</span><span class="sxs-lookup"><span data-stu-id="397b8-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="397b8-140">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="397b8-140">Redistributable</span></span><br/> | <span data-ttu-id="397b8-141">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="397b8-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="397b8-142">Encabezado</span><span class="sxs-lookup"><span data-stu-id="397b8-142">Header</span></span><br/>          | <dl> <span data-ttu-id="397b8-143"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="397b8-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
