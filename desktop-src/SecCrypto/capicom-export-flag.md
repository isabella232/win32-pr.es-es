---
description: El tipo de enumeración de la marca de exportación de CAPICOM \_ \_ define si se omiten los errores de exportación de clave privada.
ms.assetid: 12e6862b-5c73-4e45-8829-8086048e94f3
title: Enumeración CAPICOM_EXPORT_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EXPORT_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: fe99b1123ae35083e5c59df37234821efd2db208
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670783"
---
# <a name="capicom_export_flag-enumeration"></a><span data-ttu-id="691b7-103">\_Enumeración de marcas de exportación de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="691b7-103">CAPICOM\_EXPORT\_FLAG enumeration</span></span>

<span data-ttu-id="691b7-104">El tipo de enumeración de la **\_ \_ marca de exportación de CAPICOM** define si se omiten los errores de exportación de clave privada.</span><span class="sxs-lookup"><span data-stu-id="691b7-104">The **CAPICOM\_EXPORT\_FLAG** enumeration type defines whether any private key export errors are ignored.</span></span>

## <a name="members"></a><span data-ttu-id="691b7-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="691b7-105">Members</span></span>



| <span data-ttu-id="691b7-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="691b7-106">Member</span></span>                                                            | <span data-ttu-id="691b7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="691b7-107">Description</span></span>                                               | <span data-ttu-id="691b7-108">Value</span><span class="sxs-lookup"><span data-stu-id="691b7-108">Value</span></span> |
|-------------------------------------------------------------------|-----------------------------------------------------------|-------|
| <span data-ttu-id="691b7-109">**\_ \_ configuración predeterminada de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="691b7-109">**CAPICOM\_EXPORT\_DEFAULT**</span></span>                                      | <span data-ttu-id="691b7-110">Los errores de exportación de claves privadas no se pasan por alto.</span><span class="sxs-lookup"><span data-stu-id="691b7-110">Any private key export errors are not ignored.</span></span><br/> | <span data-ttu-id="691b7-111">0</span><span class="sxs-lookup"><span data-stu-id="691b7-111">0</span></span>     |
| <span data-ttu-id="691b7-112">**ERROR de exportación de CAPICOM \_ \_ omitir \_ \_ clave privada \_ no \_ exportable \_**</span><span class="sxs-lookup"><span data-stu-id="691b7-112">**CAPICOM\_EXPORT\_IGNORE\_PRIVATE\_KEY\_NOT\_EXPORTABLE\_ERROR**</span></span> | <span data-ttu-id="691b7-113">Se omiten los errores de exportación de claves privadas.</span><span class="sxs-lookup"><span data-stu-id="691b7-113">Any private key export errors are ignored.</span></span><br/>     | <span data-ttu-id="691b7-114">1</span><span class="sxs-lookup"><span data-stu-id="691b7-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="691b7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="691b7-115">Remarks</span></span>

<span data-ttu-id="691b7-116">El tipo de enumeración de la marca de exportación de CAPICOM \_ \_ se usa en el método siguiente:</span><span class="sxs-lookup"><span data-stu-id="691b7-116">The CAPICOM\_EXPORT\_FLAG enumeration type is used by the following method:</span></span>

-   [<span data-ttu-id="691b7-117">**Certificados. guardar**</span><span class="sxs-lookup"><span data-stu-id="691b7-117">**Certificates.Save**</span></span>](certificates-save.md)

## <a name="requirements"></a><span data-ttu-id="691b7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="691b7-118">Requirements</span></span>



| <span data-ttu-id="691b7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="691b7-119">Requirement</span></span> | <span data-ttu-id="691b7-120">Value</span><span class="sxs-lookup"><span data-stu-id="691b7-120">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="691b7-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="691b7-121">Redistributable</span></span><br/> | <span data-ttu-id="691b7-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="691b7-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="691b7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="691b7-123">Header</span></span><br/>          | <dl> <span data-ttu-id="691b7-124"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="691b7-124"><dt>Capicom.h</dt></span></span> </dl> |



 

 




