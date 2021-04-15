---
title: Estructura de WINBIO_VERSION (Winbio \_ Types. h)
description: Contiene el número de versión de software de un componente de proveedor de servicios biométricos.
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- Plataforma de biometría de Windows API de WINBIO_VERSION Structure
- PWINBIO_VERSION de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7d9cda802e89006ed49f6ec4b4e96c88602c511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493018"
---
# <a name="winbio_version-structure"></a><span data-ttu-id="552ac-105">Estructura de la versión de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="552ac-105">WINBIO\_VERSION structure</span></span>

<span data-ttu-id="552ac-106">La estructura de la **\_ versión WINBIO** contiene el número de versión de software de un componente de proveedor de servicios biométricos.</span><span class="sxs-lookup"><span data-stu-id="552ac-106">The **WINBIO\_VERSION** structure contains the software version number of a biometric service provider component.</span></span>

## <a name="syntax"></a><span data-ttu-id="552ac-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="552ac-107">Syntax</span></span>


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a><span data-ttu-id="552ac-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="552ac-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="552ac-109">**MajorVersion**</span><span class="sxs-lookup"><span data-stu-id="552ac-109">**MajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="552ac-110">**DWORD** que contiene el número de versión principal.</span><span class="sxs-lookup"><span data-stu-id="552ac-110">A **DWORD** that contains the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="552ac-111">**MinorVersion**</span><span class="sxs-lookup"><span data-stu-id="552ac-111">**MinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="552ac-112">**DWORD** que contiene el número de versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="552ac-112">A **DWORD** that contains the minor version number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="552ac-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="552ac-113">Requirements</span></span>



| <span data-ttu-id="552ac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="552ac-114">Requirement</span></span> | <span data-ttu-id="552ac-115">Value</span><span class="sxs-lookup"><span data-stu-id="552ac-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552ac-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="552ac-116">Minimum supported client</span></span><br/> | <span data-ttu-id="552ac-117">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="552ac-117">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="552ac-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="552ac-118">Minimum supported server</span></span><br/> | <span data-ttu-id="552ac-119">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="552ac-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="552ac-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="552ac-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="552ac-121"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="552ac-121"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="552ac-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="552ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="552ac-123">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="552ac-123">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="552ac-124">**\_esquema BSP de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="552ac-124">**WINBIO\_BSP\_SCHEMA**</span></span>](winbio-bsp-schema.md)
</dt> <dt>

[<span data-ttu-id="552ac-125">**esquema de la \_ unidad WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="552ac-125">**WINBIO\_UNIT\_SCHEMA**</span></span>](winbio-unit-schema.md)
</dt> </dl>

 

 





