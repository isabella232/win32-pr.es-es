---
description: Asocia un nombre de grupo y su identificador.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Estructura GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666272"
---
# <a name="groupinfo-structure"></a><span data-ttu-id="0f0d1-103">Estructura GROUPINFO</span><span class="sxs-lookup"><span data-stu-id="0f0d1-103">GROUPINFO structure</span></span>

<span data-ttu-id="0f0d1-104">La estructura **GROUPINFO** asocia un nombre de grupo y su identificador.</span><span class="sxs-lookup"><span data-stu-id="0f0d1-104">The **GROUPINFO** structure associates a group name and its handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f0d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f0d1-105">Syntax</span></span>


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a><span data-ttu-id="0f0d1-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0f0d1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0f0d1-107">**szGroupName**</span><span class="sxs-lookup"><span data-stu-id="0f0d1-107">**szGroupName**</span></span>
</dt> <dd>

<span data-ttu-id="0f0d1-108">Valor incrementado de una matriz en la estructura **GROUPNAME** .</span><span class="sxs-lookup"><span data-stu-id="0f0d1-108">Incremented value of an array in the **GROUPNAME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f0d1-109">**hGroup**</span><span class="sxs-lookup"><span data-stu-id="0f0d1-109">**hGroup**</span></span>
</dt> <dd>

<span data-ttu-id="0f0d1-110">Identificador de un grupo.</span><span class="sxs-lookup"><span data-stu-id="0f0d1-110">Handle to a group.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f0d1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f0d1-111">Requirements</span></span>



| <span data-ttu-id="0f0d1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f0d1-112">Requirement</span></span> | <span data-ttu-id="0f0d1-113">Value</span><span class="sxs-lookup"><span data-stu-id="0f0d1-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f0d1-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f0d1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0f0d1-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0f0d1-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f0d1-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f0d1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0f0d1-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0f0d1-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f0d1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f0d1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f0d1-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f0d1-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




