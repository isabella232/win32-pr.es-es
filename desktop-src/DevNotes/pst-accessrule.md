---
description: Describe una regla para el acceso a los elementos almacenados en el almacenamiento protegido.
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: PST_ACCESSRULE estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 90a04f2f7a34874a8c076fa55b158944399fac2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650025"
---
# <a name="pst_accessrule-structure"></a><span data-ttu-id="d4ff1-103">\_Estructura ACCESSRULE de PST</span><span class="sxs-lookup"><span data-stu-id="d4ff1-103">PST\_ACCESSRULE structure</span></span>

<span data-ttu-id="d4ff1-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="d4ff1-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="d4ff1-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="d4ff1-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="d4ff1-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="d4ff1-108">Describe una regla para el acceso a los elementos almacenados en el almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-108">Describes a rule for access to items stored in protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4ff1-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4ff1-109">Syntax</span></span>


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a><span data-ttu-id="d4ff1-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4ff1-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4ff1-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="d4ff1-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="d4ff1-112">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="d4ff1-113">**AccessModeFlags**</span><span class="sxs-lookup"><span data-stu-id="d4ff1-113">**AccessModeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d4ff1-114">Los modos de acceso a los que pertenece un conjunto especificado de cláusulas de acceso.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-114">The access modes to which a specified set of access clauses pertain.</span></span>



| <span data-ttu-id="d4ff1-115">Value</span><span class="sxs-lookup"><span data-stu-id="d4ff1-115">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="d4ff1-116">Significado</span><span class="sxs-lookup"><span data-stu-id="d4ff1-116">Meaning</span></span>                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <span data-ttu-id="d4ff1-117"><dt>**Archivo pst \_ LEER**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="d4ff1-117"><dt>**PST\_READ**</dt> <dt>0x0001</dt></span></span> </dl>    | <span data-ttu-id="d4ff1-118">Modo de acceso de lectura.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-118">Read access mode.</span></span><br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <span data-ttu-id="d4ff1-119"><dt>**Archivo pst \_ ESCRIBIR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="d4ff1-119"><dt>**PST\_WRITE**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="d4ff1-120">Modo de acceso de escritura.</span><span class="sxs-lookup"><span data-stu-id="d4ff1-120">Write access mode.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4ff1-121">**cClauses**</span><span class="sxs-lookup"><span data-stu-id="d4ff1-121">**cClauses**</span></span>
</dt> <dd>

<span data-ttu-id="d4ff1-122">El número de estructuras de la matriz **rgClauses** .</span><span class="sxs-lookup"><span data-stu-id="d4ff1-122">The number of structures in the **rgClauses** array.</span></span>

</dd> <dt>

<span data-ttu-id="d4ff1-123">**rgClauses**</span><span class="sxs-lookup"><span data-stu-id="d4ff1-123">**rgClauses**</span></span>
</dt> <dd>

<span data-ttu-id="d4ff1-124">Puntero a una matriz de estructuras [**\_ ACCESSCLAUSE de PST**](pst-accessclause.md) .</span><span class="sxs-lookup"><span data-stu-id="d4ff1-124">A pointer to an array of [**PST\_ACCESSCLAUSE**](pst-accessclause.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4ff1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4ff1-125">Requirements</span></span>



| <span data-ttu-id="d4ff1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4ff1-126">Requirement</span></span> | <span data-ttu-id="d4ff1-127">Value</span><span class="sxs-lookup"><span data-stu-id="d4ff1-127">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d4ff1-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d4ff1-128">Header</span></span><br/> | <dl> <span data-ttu-id="d4ff1-129"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4ff1-129"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ff1-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4ff1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ff1-131">**PST \_ ACCESSCLAUSE**</span><span class="sxs-lookup"><span data-stu-id="d4ff1-131">**PST\_ACCESSCLAUSE**</span></span>](pst-accessclause.md)
</dt> <dt>

[<span data-ttu-id="d4ff1-132">**PST \_ ACCESSRULESET**</span><span class="sxs-lookup"><span data-stu-id="d4ff1-132">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> </dl>

 

 
