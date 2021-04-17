---
description: Indica la ubicación en la que se buscará un almacén de certificados Active Directory.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Enumeración CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cd630bdc0c09a6bb57a9163ec972451011f3e826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670614"
---
# <a name="capicom_active_directory_search_location-enumeration"></a><span data-ttu-id="4e05c-103">CAPICOM \_ Active \_ Directory \_ Search \_ Location (enumeración)</span><span class="sxs-lookup"><span data-stu-id="4e05c-103">CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION enumeration</span></span>

<span data-ttu-id="4e05c-104">El tipo de enumeración ubicación de **\_ búsqueda de Active \_ Directory \_ \_ de CAPICOM** indica la ubicación en la que se buscará un almacén de [*certificados*](../secgloss/c-gly.md)Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4e05c-104">The **CAPICOM\_ACTIVE\_DIRECTORY\_SEARCH\_LOCATION** enumeration type indicates the location to be searched for an Active Directory [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="4e05c-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="4e05c-105">Members</span></span>



| <span data-ttu-id="4e05c-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="4e05c-106">Member</span></span>                               | <span data-ttu-id="4e05c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e05c-107">Description</span></span>                                  | <span data-ttu-id="4e05c-108">Value</span><span class="sxs-lookup"><span data-stu-id="4e05c-108">Value</span></span> |
|--------------------------------------|----------------------------------------------|-------|
| <span data-ttu-id="4e05c-109">**CAPICOM \_ Search \_ any**</span><span class="sxs-lookup"><span data-stu-id="4e05c-109">**CAPICOM\_SEARCH\_ANY**</span></span>             | <span data-ttu-id="4e05c-110">Busca en todas las ubicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="4e05c-110">Searches all available locations.</span></span><br/> | <span data-ttu-id="4e05c-111">0</span><span class="sxs-lookup"><span data-stu-id="4e05c-111">0</span></span>     |
| <span data-ttu-id="4e05c-112">**CAPICOM \_ Buscar en el \_ \_ catálogo global**</span><span class="sxs-lookup"><span data-stu-id="4e05c-112">**CAPICOM\_SEARCH\_GLOBAL\_CATALOG**</span></span> | <span data-ttu-id="4e05c-113">Busca solo en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="4e05c-113">Searches only the global catalog.</span></span><br/> | <span data-ttu-id="4e05c-114">1</span><span class="sxs-lookup"><span data-stu-id="4e05c-114">1</span></span>     |
| <span data-ttu-id="4e05c-115">**\_ \_ dominio predeterminado de búsqueda de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="4e05c-115">**CAPICOM\_SEARCH\_DEFAULT\_DOMAIN**</span></span> | <span data-ttu-id="4e05c-116">Busca solo en el dominio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4e05c-116">Searches only the default domain.</span></span><br/> | <span data-ttu-id="4e05c-117">2</span><span class="sxs-lookup"><span data-stu-id="4e05c-117">2</span></span>     |



## <a name="remarks"></a><span data-ttu-id="4e05c-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e05c-118">Remarks</span></span>

<span data-ttu-id="4e05c-119">Este tipo de enumeración se usa en la siguiente propiedad:</span><span class="sxs-lookup"><span data-stu-id="4e05c-119">This enumeration type is used by the following property:</span></span>

-   [<span data-ttu-id="4e05c-120">**Settings. ActiveDirectorySearchLocation**</span><span class="sxs-lookup"><span data-stu-id="4e05c-120">**Settings.ActiveDirectorySearchLocation**</span></span>](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a><span data-ttu-id="4e05c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e05c-121">Requirements</span></span>



| <span data-ttu-id="4e05c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e05c-122">Requirement</span></span> | <span data-ttu-id="4e05c-123">Value</span><span class="sxs-lookup"><span data-stu-id="4e05c-123">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4e05c-124">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4e05c-124">Redistributable</span></span><br/> | <span data-ttu-id="4e05c-125">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4e05c-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="4e05c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e05c-126">Header</span></span><br/>          | <dl> <span data-ttu-id="4e05c-127"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e05c-127"><dt>Capicom.h</dt></span></span> </dl> |



 

 
