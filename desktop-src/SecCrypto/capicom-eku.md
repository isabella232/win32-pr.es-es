---
description: Define los nombres de uso de clave extendidos en función de dónde se pueden usar.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Enumeración CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670852"
---
# <a name="capicom_eku-enumeration"></a><span data-ttu-id="cde64-103">\_Enumeración de EKU de CAPICOM</span><span class="sxs-lookup"><span data-stu-id="cde64-103">CAPICOM\_EKU enumeration</span></span>

<span data-ttu-id="cde64-104">El tipo de enumeración **\_ EKU de CAPICOM** define los nombres de uso de clave extendidos en función de dónde se pueden usar.</span><span class="sxs-lookup"><span data-stu-id="cde64-104">The **CAPICOM\_EKU** enumeration type defines the extended key usage names based on where they can be used.</span></span>

## <a name="members"></a><span data-ttu-id="cde64-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="cde64-105">Members</span></span>



| <span data-ttu-id="cde64-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="cde64-106">Member</span></span>                                     | <span data-ttu-id="cde64-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cde64-107">Description</span></span>                                                                                                                                                 | <span data-ttu-id="cde64-108">Value</span><span class="sxs-lookup"><span data-stu-id="cde64-108">Value</span></span> |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="cde64-109">**EKU de CAPICOM \_ \_ otro**</span><span class="sxs-lookup"><span data-stu-id="cde64-109">**CAPICOM\_EKU\_OTHER**</span></span>                    | <span data-ttu-id="cde64-110">El certificado tiene usos definidos en la directiva local.</span><span class="sxs-lookup"><span data-stu-id="cde64-110">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="cde64-111">Se usa si el EKU necesario no está predefinido y la aplicación debe establecer el valor de OID.</span><span class="sxs-lookup"><span data-stu-id="cde64-111">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> | <span data-ttu-id="cde64-112">0</span><span class="sxs-lookup"><span data-stu-id="cde64-112">0</span></span>     |
| <span data-ttu-id="cde64-113">**\_autenticación del \_ servidor \_ EKU de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="cde64-113">**CAPICOM\_EKU\_SERVER\_AUTH**</span></span>             | <span data-ttu-id="cde64-114">El certificado se puede usar para autenticar un servidor.</span><span class="sxs-lookup"><span data-stu-id="cde64-114">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                | <span data-ttu-id="cde64-115">1</span><span class="sxs-lookup"><span data-stu-id="cde64-115">1</span></span>     |
| <span data-ttu-id="cde64-116">**\_autenticación de \_ cliente de EKU de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="cde64-116">**CAPICOM\_EKU\_CLIENT\_AUTH**</span></span>             | <span data-ttu-id="cde64-117">El certificado se puede utilizar para autenticar a un cliente.</span><span class="sxs-lookup"><span data-stu-id="cde64-117">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                | <span data-ttu-id="cde64-118">2</span><span class="sxs-lookup"><span data-stu-id="cde64-118">2</span></span>     |
| <span data-ttu-id="cde64-119">**\_firma de \_ código \_ EKU de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="cde64-119">**CAPICOM\_EKU\_CODE\_SIGNING**</span></span>            | <span data-ttu-id="cde64-120">El certificado se puede utilizar para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="cde64-120">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           | <span data-ttu-id="cde64-121">3</span><span class="sxs-lookup"><span data-stu-id="cde64-121">3</span></span>     |
| <span data-ttu-id="cde64-122">**\_protección de \_ correo electrónico de EKU de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="cde64-122">**CAPICOM\_EKU\_EMAIL\_PROTECTION**</span></span>        | <span data-ttu-id="cde64-123">El certificado se puede usar para la protección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cde64-123">Certificate can be used for email protection.</span></span><br/>                                                                                                    | <span data-ttu-id="cde64-124">4</span><span class="sxs-lookup"><span data-stu-id="cde64-124">4</span></span>     |
| <span data-ttu-id="cde64-125">**\_Inicio de \_ sesión con tarjeta inteligente EKU de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="cde64-125">**CAPICOM\_EKU\_SMARTCARD\_LOGON**</span></span>         | <span data-ttu-id="cde64-126">El certificado se puede usar para el inicio de sesión con tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="cde64-126">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="cde64-127">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cde64-127">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         | <span data-ttu-id="cde64-128">5</span><span class="sxs-lookup"><span data-stu-id="cde64-128">5</span></span>     |
| <span data-ttu-id="cde64-129">**\_sistema de \_ cifrado de \_ archivos \_ EKU de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="cde64-129">**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</span></span> | <span data-ttu-id="cde64-130">El certificado se puede usar para EFS.</span><span class="sxs-lookup"><span data-stu-id="cde64-130">Certificate can be used for EFS.</span></span> <span data-ttu-id="cde64-131">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="cde64-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      | <span data-ttu-id="cde64-132">6</span><span class="sxs-lookup"><span data-stu-id="cde64-132">6</span></span>     |



## <a name="remarks"></a><span data-ttu-id="cde64-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cde64-133">Remarks</span></span>

<span data-ttu-id="cde64-134">El EKU usa el tipo de enumeración **\_ EKU de CAPICOM** [**. Propiedad nombre**](eku-name.md) .</span><span class="sxs-lookup"><span data-stu-id="cde64-134">The **CAPICOM\_EKU** enumeration type is used by the [**EKU.Name**](eku-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="cde64-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cde64-135">Requirements</span></span>



| <span data-ttu-id="cde64-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde64-136">Requirement</span></span> | <span data-ttu-id="cde64-137">Value</span><span class="sxs-lookup"><span data-stu-id="cde64-137">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cde64-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="cde64-138">Redistributable</span></span><br/> | <span data-ttu-id="cde64-139">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="cde64-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="cde64-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cde64-140">Header</span></span><br/>          | <dl> <span data-ttu-id="cde64-141"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde64-141"><dt>Capicom.h</dt></span></span> </dl> |



 

 




