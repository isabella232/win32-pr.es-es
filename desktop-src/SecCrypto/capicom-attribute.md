---
description: Define el tipo de atributo asociado a una firma.
ms.assetid: 94f0dce4-0b32-4c39-ab2e-b01795432acd
title: Enumeración CAPICOM_ATTRIBUTE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ATTRIBUTE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: b03f91d0737b29b98adeb7e6a56bf9eccd35cc8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671471"
---
# <a name="capicom_attribute-enumeration"></a><span data-ttu-id="21955-103">CAPICOM \_ (enumeración de atributos)</span><span class="sxs-lookup"><span data-stu-id="21955-103">CAPICOM\_ATTRIBUTE enumeration</span></span>

<span data-ttu-id="21955-104">El tipo de enumeración del **\_ atributo CAPICOM** define el tipo de atributo asociado a una [*firma*](../secgloss/d-gly.md).</span><span class="sxs-lookup"><span data-stu-id="21955-104">The **CAPICOM\_ATTRIBUTE** enumeration type defines the kind of attribute associated with a [*signature*](../secgloss/d-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="21955-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="21955-105">Members</span></span>



| <span data-ttu-id="21955-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="21955-106">Member</span></span>                                                       | <span data-ttu-id="21955-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="21955-107">Description</span></span>                                                                | <span data-ttu-id="21955-108">Value</span><span class="sxs-lookup"><span data-stu-id="21955-108">Value</span></span> |
|--------------------------------------------------------------|----------------------------------------------------------------------------|-------|
| <span data-ttu-id="21955-109">**\_tiempo de firma de atributo autenticado de CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21955-109">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</span></span>         | <span data-ttu-id="21955-110">El atributo contiene la hora a la que se creó la firma.</span><span class="sxs-lookup"><span data-stu-id="21955-110">The attribute contains the time that the signature was created.</span></span><br/> | <span data-ttu-id="21955-111">0</span><span class="sxs-lookup"><span data-stu-id="21955-111">0</span></span>     |
| <span data-ttu-id="21955-112">**\_nombre de documento de atributo autenticado de CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21955-112">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</span></span>        | <span data-ttu-id="21955-113">El atributo contiene el nombre del documento firmado.</span><span class="sxs-lookup"><span data-stu-id="21955-113">The attribute contains the name of the signed document.</span></span><br/>         | <span data-ttu-id="21955-114">1</span><span class="sxs-lookup"><span data-stu-id="21955-114">1</span></span>     |
| <span data-ttu-id="21955-115">**\_Descripción del documento de atributo autenticado de CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="21955-115">**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</span></span> | <span data-ttu-id="21955-116">El atributo contiene una descripción del documento firmado.</span><span class="sxs-lookup"><span data-stu-id="21955-116">The attribute contains a description of the signed document.</span></span><br/>    | <span data-ttu-id="21955-117">2</span><span class="sxs-lookup"><span data-stu-id="21955-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="21955-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21955-118">Remarks</span></span>

<span data-ttu-id="21955-119">La propiedad [**Attribute.Name**](attribute-name.md) usa el tipo de enumeración del **\_ atributo CAPICOM** .</span><span class="sxs-lookup"><span data-stu-id="21955-119">The **CAPICOM\_ATTRIBUTE** enumeration type is used by the [**Attribute.Name**](attribute-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="21955-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21955-120">Requirements</span></span>



| <span data-ttu-id="21955-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21955-121">Requirement</span></span> | <span data-ttu-id="21955-122">Value</span><span class="sxs-lookup"><span data-stu-id="21955-122">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21955-123">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="21955-123">Redistributable</span></span><br/> | <span data-ttu-id="21955-124">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="21955-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="21955-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="21955-125">Header</span></span><br/>          | <dl> <span data-ttu-id="21955-126"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="21955-126"><dt>Capicom.h</dt></span></span> </dl> |



 

 
