---
title: Estructura de WINBIO_BSP_SCHEMA (Winbio \_ Types. h)
description: Describe las capacidades de un proveedor de servicios biométricos.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- Plataforma de biometría de Windows API de WINBIO_BSP_SCHEMA Structure
- PWINBIO_BSP_SCHEMA de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490768"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="3a606-105">\_Estructura de esquema BSP de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3a606-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="3a606-106">La estructura de **\_ \_ esquema BSP de WINBIO** describe las capacidades de un proveedor de servicios biométricos.</span><span class="sxs-lookup"><span data-stu-id="3a606-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="3a606-107">La función [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="3a606-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a606-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a606-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="3a606-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a606-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="3a606-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="3a606-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="3a606-111">Tipo de medida biométrica usada por este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3a606-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="3a606-112">Actualmente, este debe ser **WINBIO \_ tipo de \_ huella digital**.</span><span class="sxs-lookup"><span data-stu-id="3a606-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="3a606-113">**BspId**</span><span class="sxs-lookup"><span data-stu-id="3a606-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="3a606-114">Valor que identifica de forma única este componente de proveedor de servicios biométricos.</span><span class="sxs-lookup"><span data-stu-id="3a606-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="3a606-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a606-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3a606-116">Una cadena Unicode terminada en **null** que contiene una descripción del proveedor de servicios biométricos.</span><span class="sxs-lookup"><span data-stu-id="3a606-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="3a606-117">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="3a606-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="3a606-118">Una cadena Unicode terminada en **null** que contiene el nombre del proveedor que proporciona el proveedor de servicios biométricos.</span><span class="sxs-lookup"><span data-stu-id="3a606-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="3a606-119">**Versión**</span><span class="sxs-lookup"><span data-stu-id="3a606-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="3a606-120">Una estructura de [**\_ versión de WINBIO**](winbio-version.md) que contiene la versión de software del componente de proveedor de servicios biométricos.</span><span class="sxs-lookup"><span data-stu-id="3a606-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a606-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a606-121">Requirements</span></span>



| <span data-ttu-id="3a606-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a606-122">Requirement</span></span> | <span data-ttu-id="3a606-123">Value</span><span class="sxs-lookup"><span data-stu-id="3a606-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a606-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a606-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3a606-125">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a606-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="3a606-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a606-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3a606-127">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a606-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3a606-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a606-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a606-129"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a606-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a606-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a606-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a606-131">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="3a606-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="3a606-132">**WinBioEnumServiceProviders**</span><span class="sxs-lookup"><span data-stu-id="3a606-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





