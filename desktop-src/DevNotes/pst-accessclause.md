---
description: Contiene información sobre la cláusula de acceso para el almacenamiento protegido.
ms.assetid: 59634ada-4879-4ae7-b757-dfa6a88549af
title: PST_ACCESSCLAUSE estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSCLAUSE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 3536b92bf1d014090f124976b8f4a16e25beb444
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670511"
---
# <a name="pst_accessclause-structure"></a><span data-ttu-id="bc8db-103">\_Estructura ACCESSCLAUSE de PST</span><span class="sxs-lookup"><span data-stu-id="bc8db-103">PST\_ACCESSCLAUSE structure</span></span>

<span data-ttu-id="bc8db-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bc8db-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="bc8db-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="bc8db-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="bc8db-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="bc8db-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="bc8db-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="bc8db-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="bc8db-108">Contiene información sobre la cláusula de acceso para el almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="bc8db-108">Contains information about the access clause for the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc8db-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc8db-109">Syntax</span></span>


```C++
typedef struct {
  DWORD                cbSize;
  PST_ACCESSCLAUSETYPE ClauseType;
  DWORD                cbClauseData;
  BYTE                 *pbClauseData;
} PST_ACCESSCLAUSE, *PPST_ACCESSCLAUSE;
```



## <a name="members"></a><span data-ttu-id="bc8db-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc8db-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="bc8db-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="bc8db-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="bc8db-112">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bc8db-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="bc8db-113">**ClauseType**</span><span class="sxs-lookup"><span data-stu-id="bc8db-113">**ClauseType**</span></span>
</dt> <dd>

<span data-ttu-id="bc8db-114">El tipo de datos al que apunta el miembro **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="bc8db-114">The type of data that is pointed to by the **pbClauseData** member.</span></span> <span data-ttu-id="bc8db-115">Para obtener más información, vea [**PStore Types**](pstore-types.md).</span><span class="sxs-lookup"><span data-stu-id="bc8db-115">For more information, see [**PStore Types**](pstore-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="bc8db-116">**cbClauseData**</span><span class="sxs-lookup"><span data-stu-id="bc8db-116">**cbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="bc8db-117">Tamaño de los datos a los que apunta el miembro **pbClauseData** .</span><span class="sxs-lookup"><span data-stu-id="bc8db-117">The size of the data that is pointed to by the **pbClauseData** member.</span></span>

</dd> <dt>

<span data-ttu-id="bc8db-118">**pbClauseData**</span><span class="sxs-lookup"><span data-stu-id="bc8db-118">**pbClauseData**</span></span>
</dt> <dd>

<span data-ttu-id="bc8db-119">Puntero a los datos de la cláusula de acceso.</span><span class="sxs-lookup"><span data-stu-id="bc8db-119">A pointer to the access clause data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc8db-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc8db-120">Requirements</span></span>



| <span data-ttu-id="bc8db-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc8db-121">Requirement</span></span> | <span data-ttu-id="bc8db-122">Value</span><span class="sxs-lookup"><span data-stu-id="bc8db-122">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bc8db-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc8db-123">Header</span></span><br/> | <dl> <span data-ttu-id="bc8db-124"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc8db-124"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc8db-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc8db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc8db-126">**PST \_ ACCESSRULE**</span><span class="sxs-lookup"><span data-stu-id="bc8db-126">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> </dl>

 

 
