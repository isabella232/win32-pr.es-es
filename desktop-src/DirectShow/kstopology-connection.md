---
description: Este tema se aplica a Windows XP Service Pack 2 o posterior. La \_ estructura de conexión KSTOPOLOGY describe una conexión de nodo dentro de un filtro de streaming de kernel (KS). Un nodo puede estar conectado a otro nodo dentro del filtro o a un PIN en el filtro.
ms.assetid: 8fca47b7-4c52-46db-809c-77a0e3414276
title: KSTOPOLOGY_CONNECTION estructura (KS. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSTOPOLOGY_CONNECTION
api_type:
- HeaderDef
api_location:
- Ks.h
ms.openlocfilehash: f523d378a54311845781c144b33e131d5875e41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690656"
---
# <a name="kstopology_connection-structure"></a><span data-ttu-id="a0440-105">Estructura de conexión de KSTOPOLOGY \_</span><span class="sxs-lookup"><span data-stu-id="a0440-105">KSTOPOLOGY\_CONNECTION structure</span></span>

<span data-ttu-id="a0440-106">Este tema se aplica a Windows XP Service Pack 2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a0440-106">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="a0440-107">La estructura de **\_ conexión KSTOPOLOGY** describe una conexión de nodo dentro de un filtro de streaming de kernel (KS).</span><span class="sxs-lookup"><span data-stu-id="a0440-107">The **KSTOPOLOGY\_CONNECTION** structure describes a node connection within a kernel-streaming (KS) filter.</span></span> <span data-ttu-id="a0440-108">Un nodo puede estar conectado a otro nodo dentro del filtro o a un PIN en el filtro.</span><span class="sxs-lookup"><span data-stu-id="a0440-108">A node can be connected to another node within the filter, or to a pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0440-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0440-109">Syntax</span></span>


```C++
typedef struct {
  ULONG FromNode;
  ULONG FromNodePin;
  ULONG ToNode;
  ULONG ToNodePin;
} KSTOPOLOGY_CONNECTION, *PKSTOPOLOGY_CONNECTION;
```



## <a name="members"></a><span data-ttu-id="a0440-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0440-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a0440-111">**FromNode**</span><span class="sxs-lookup"><span data-stu-id="a0440-111">**FromNode**</span></span>
</dt> <dd>

<span data-ttu-id="a0440-112">Índice del nodo ascendente de la conexión.</span><span class="sxs-lookup"><span data-stu-id="a0440-112">Index of the upstream node in the connection.</span></span> <span data-ttu-id="a0440-113">Si la conexión ascendente es un PIN, en lugar de un nodo, el valor es el \_ nodo KSFILTER.</span><span class="sxs-lookup"><span data-stu-id="a0440-113">If the upstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="a0440-114">**FromNodePin**</span><span class="sxs-lookup"><span data-stu-id="a0440-114">**FromNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="a0440-115">Si el valor del campo **FromNode** es KSFILTER \_ nodo, este campo especifica el índice del PIN ascendente.</span><span class="sxs-lookup"><span data-stu-id="a0440-115">If the value of the **FromNode** field is KSFILTER\_NODE, this field specifies the index of the upstream pin.</span></span> <span data-ttu-id="a0440-116">De lo contrario, se omite este campo.</span><span class="sxs-lookup"><span data-stu-id="a0440-116">Otherwise, this field is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="a0440-117">**ToNode**</span><span class="sxs-lookup"><span data-stu-id="a0440-117">**ToNode**</span></span>
</dt> <dd>

<span data-ttu-id="a0440-118">Índice del nodo de nivel inferior en la conexión.</span><span class="sxs-lookup"><span data-stu-id="a0440-118">Index of the downstream node in the connection.</span></span> <span data-ttu-id="a0440-119">Si la conexión de bajada es un PIN, en lugar de un nodo, el valor es el \_ nodo KSFILTER.</span><span class="sxs-lookup"><span data-stu-id="a0440-119">If the downstream connection is a pin, rather than a node, the value is KSFILTER\_NODE.</span></span>

</dd> <dt>

<span data-ttu-id="a0440-120">**ToNodePin**</span><span class="sxs-lookup"><span data-stu-id="a0440-120">**ToNodePin**</span></span>
</dt> <dd>

<span data-ttu-id="a0440-121">Si el valor del campo **ToNode** es KSFILTER \_ nodo, este campo especifica el índice del código PIN de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="a0440-121">If the value of the **ToNode** field is KSFILTER\_NODE, this field specifies the index of the downstream pin.</span></span> <span data-ttu-id="a0440-122">De lo contrario, se omite este campo.</span><span class="sxs-lookup"><span data-stu-id="a0440-122">Otherwise, this field is ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0440-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0440-123">Requirements</span></span>



| <span data-ttu-id="a0440-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0440-124">Requirement</span></span> | <span data-ttu-id="a0440-125">Value</span><span class="sxs-lookup"><span data-stu-id="a0440-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a0440-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a0440-126">Header</span></span><br/> | <dl> <span data-ttu-id="a0440-127"><dt>KS. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0440-127"><dt>Ks.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0440-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0440-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0440-129">Estructuras de DirectShow</span><span class="sxs-lookup"><span data-stu-id="a0440-129">DirectShow Structures</span></span>](directshow-structures.md)
</dt> <dt>

[<span data-ttu-id="a0440-130">**IKsTopologyInfo:: get \_ ConnectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a0440-130">**IKsTopologyInfo::get\_ConnectionInfo**</span></span>](/previous-versions/windows/desktop/api/Vidcap/nf-vidcap-ikstopologyinfo-get_connectioninfo)
</dt> </dl>

 

 




