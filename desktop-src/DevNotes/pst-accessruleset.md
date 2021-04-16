---
description: Identifica el conjunto de reglas de acceso para los datos de almacenamiento protegido.
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: PST_ACCESSRULESET estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671428"
---
# <a name="pst_accessruleset-structure"></a><span data-ttu-id="fd99b-103">\_Estructura ACCESSRULESET de PST</span><span class="sxs-lookup"><span data-stu-id="fd99b-103">PST\_ACCESSRULESET structure</span></span>

<span data-ttu-id="fd99b-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd99b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="fd99b-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="fd99b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="fd99b-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="fd99b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="fd99b-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="fd99b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="fd99b-108">Identifica el conjunto de reglas de acceso para los datos de almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="fd99b-108">Identifies the set of access rules for the protected storage data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd99b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd99b-109">Syntax</span></span>


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a><span data-ttu-id="fd99b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd99b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="fd99b-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="fd99b-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="fd99b-112">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="fd99b-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="fd99b-113">**cRules**</span><span class="sxs-lookup"><span data-stu-id="fd99b-113">**cRules**</span></span>
</dt> <dd>

<span data-ttu-id="fd99b-114">El número de reglas de la matriz **rgRules** .</span><span class="sxs-lookup"><span data-stu-id="fd99b-114">The number of rules in the **rgRules** array.</span></span>

</dd> <dt>

<span data-ttu-id="fd99b-115">**rgRules**</span><span class="sxs-lookup"><span data-stu-id="fd99b-115">**rgRules**</span></span>
</dt> <dd>

<span data-ttu-id="fd99b-116">Puntero a una matriz de estructuras [**\_ ACCESSRULE de PST**](pst-accessrule.md) .</span><span class="sxs-lookup"><span data-stu-id="fd99b-116">A pointer to an array of [**PST\_ACCESSRULE**](pst-accessrule.md) structures.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd99b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd99b-117">Requirements</span></span>



| <span data-ttu-id="fd99b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd99b-118">Requirement</span></span> | <span data-ttu-id="fd99b-119">Value</span><span class="sxs-lookup"><span data-stu-id="fd99b-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fd99b-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd99b-120">Header</span></span><br/> | <dl> <span data-ttu-id="fd99b-121"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd99b-121"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd99b-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd99b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd99b-123">**PST \_ ACCESSRULE**</span><span class="sxs-lookup"><span data-stu-id="fd99b-123">**PST\_ACCESSRULE**</span></span>](pst-accessrule.md)
</dt> <dt>

[<span data-ttu-id="fd99b-124">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="fd99b-124">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> </dl>

 

 
