---
description: Empaqueta la información sobre el tipo de objeto, la versión y el tamaño necesaria en muchas estructuras NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER estructura (Ntddndis. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687434"
---
# <a name="ndis_object_header-structure"></a><span data-ttu-id="5ab54-103">Estructura de encabezado de \_ objeto NDIS \_</span><span class="sxs-lookup"><span data-stu-id="5ab54-103">NDIS\_OBJECT\_HEADER structure</span></span>

<span data-ttu-id="5ab54-104">La estructura de **\_ \_ encabezado de objeto NDIS** empaqueta la información sobre el tipo de objeto, la versión y el tamaño necesaria en muchas estructuras NDIS 6,0.</span><span class="sxs-lookup"><span data-stu-id="5ab54-104">The **NDIS\_OBJECT\_HEADER** structure packages the object type, version, and size information that is required in many NDIS 6.0 structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ab54-105">Syntax</span></span>


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a><span data-ttu-id="5ab54-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5ab54-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5ab54-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="5ab54-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="5ab54-108">Especifica el tipo de objeto NDIS que describe una estructura.</span><span class="sxs-lookup"><span data-stu-id="5ab54-108">Specifies the type of NDIS object that a structure describes.</span></span>

</dd> <dt>

<span data-ttu-id="5ab54-109">**Revisión**</span><span class="sxs-lookup"><span data-stu-id="5ab54-109">**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="5ab54-110">Especifica el número de revisión de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="5ab54-110">Specifies the revision number of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="5ab54-111">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="5ab54-111">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="5ab54-112">Especifica el tamaño total, en bytes, de la estructura NDIS que contiene el **\_ \_ encabezado de objeto NDIS**.</span><span class="sxs-lookup"><span data-stu-id="5ab54-112">Specifies the total size, in bytes, of the NDIS structure that contains the **NDIS\_OBJECT\_HEADER**.</span></span> <span data-ttu-id="5ab54-113">Este tamaño incluye el tamaño del miembro **de \_ \_ encabezado de objeto NDIS** y de todos los demás miembros de la estructura.</span><span class="sxs-lookup"><span data-stu-id="5ab54-113">This size includes the size of the **NDIS\_OBJECT\_HEADER** member and all other members of the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ab54-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ab54-114">Requirements</span></span>



| <span data-ttu-id="5ab54-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ab54-115">Requirement</span></span> | <span data-ttu-id="5ab54-116">Value</span><span class="sxs-lookup"><span data-stu-id="5ab54-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab54-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ab54-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab54-118">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="5ab54-118">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ab54-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ab54-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab54-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5ab54-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5ab54-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5ab54-121">Redistributable</span></span><br/>          | <span data-ttu-id="5ab54-122">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="5ab54-122">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="5ab54-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ab54-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ab54-124"><dt>Ntddndis. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ab54-124"><dt>Ntddndis.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ab54-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ab54-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab54-126">**\_Lista de BSSID de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="5ab54-126">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> </dl>

 

 




