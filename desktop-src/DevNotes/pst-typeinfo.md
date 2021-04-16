---
description: Describe un tipo o un subtipo.
ms.assetid: 4b6b77d9-54ea-4101-9c8b-e525f9aa3816
title: PST_TYPEINFO estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_TYPEINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: fc78d0570ff2e5cf66a9048d64143149564a51c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650069"
---
# <a name="pst_typeinfo-structure"></a><span data-ttu-id="a336a-103">PST de la \_ estructura de TYPEINFO</span><span class="sxs-lookup"><span data-stu-id="a336a-103">PST\_TYPEINFO structure</span></span>

<span data-ttu-id="a336a-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a336a-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="a336a-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="a336a-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="a336a-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="a336a-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="a336a-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="a336a-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="a336a-108">Describe un tipo o un subtipo.</span><span class="sxs-lookup"><span data-stu-id="a336a-108">Describes a type or a subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="a336a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a336a-109">Syntax</span></span>


```C++
typedef struct {
  DWORD  cbSize;
  LPWSTR szDisplayName;
} PST_TYPEINFO, *PPST_TYPEINFO;
```



## <a name="members"></a><span data-ttu-id="a336a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a336a-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="a336a-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="a336a-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="a336a-112">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="a336a-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="a336a-113">**szDisplayName**</span><span class="sxs-lookup"><span data-stu-id="a336a-113">**szDisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="a336a-114">Puntero a una cadena de caracteres anchos que representa el nombre para mostrar del tipo.</span><span class="sxs-lookup"><span data-stu-id="a336a-114">A pointer to a wide character string that represents the display name for the type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a336a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a336a-115">Requirements</span></span>



| <span data-ttu-id="a336a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a336a-116">Requirement</span></span> | <span data-ttu-id="a336a-117">Value</span><span class="sxs-lookup"><span data-stu-id="a336a-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a336a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a336a-118">Header</span></span><br/> | <dl> <span data-ttu-id="a336a-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="a336a-119"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a336a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="a336a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a336a-121">**CreateSubtype**</span><span class="sxs-lookup"><span data-stu-id="a336a-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)
</dt> <dt>

[<span data-ttu-id="a336a-122">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="a336a-122">**CreateType**</span></span>](ipstore-createtype.md)
</dt> <dt>

[<span data-ttu-id="a336a-123">**GetSubtypeInfo**</span><span class="sxs-lookup"><span data-stu-id="a336a-123">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)
</dt> <dt>

[<span data-ttu-id="a336a-124">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="a336a-124">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)
</dt> </dl>

 

 
