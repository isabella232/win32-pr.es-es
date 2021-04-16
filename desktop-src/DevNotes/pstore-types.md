---
description: Los tipos de datos para los métodos de almacenamiento protegido.
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: PStore (tipos) (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1c93af4ae6756a6489b828c50bac505241bdd3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649828"
---
# <a name="pstore-types"></a><span data-ttu-id="dbfdd-103">PStore (tipos)</span><span class="sxs-lookup"><span data-stu-id="dbfdd-103">PStore Types</span></span>

<span data-ttu-id="dbfdd-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="dbfdd-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="dbfdd-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="dbfdd-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="dbfdd-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="dbfdd-108">Los tipos de datos para los métodos de almacenamiento protegido.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-108">The data types for Protected Storage methods.</span></span>


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

<span data-ttu-id="dbfdd-109">**PST \_ ACCESSMODE**</span><span class="sxs-lookup"><span data-stu-id="dbfdd-109">**PST\_ACCESSMODE**</span></span>
</dt> <dd>

<span data-ttu-id="dbfdd-110">Define el modo de lectura o escritura de la regla de acceso.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-110">Defines the read or write mode of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="dbfdd-111">**PST \_ ACCESSCLAUSETYPE**</span><span class="sxs-lookup"><span data-stu-id="dbfdd-111">**PST\_ACCESSCLAUSETYPE**</span></span>
</dt> <dd>

<span data-ttu-id="dbfdd-112">Define el tipo de cláusula de la regla de acceso.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-112">Defines the clause type of the access rule.</span></span>

</dd> <dt>

<span data-ttu-id="dbfdd-113">**\_clave PST**</span><span class="sxs-lookup"><span data-stu-id="dbfdd-113">**PST\_KEY**</span></span>
</dt> <dd>

<span data-ttu-id="dbfdd-114">Define la clave para el elemento almacenado.</span><span class="sxs-lookup"><span data-stu-id="dbfdd-114">Defines the key for the stored item.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dbfdd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dbfdd-115">Requirements</span></span>



| <span data-ttu-id="dbfdd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dbfdd-116">Requirement</span></span> | <span data-ttu-id="dbfdd-117">Value</span><span class="sxs-lookup"><span data-stu-id="dbfdd-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dbfdd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbfdd-118">Header</span></span><br/> | <dl> <span data-ttu-id="dbfdd-119"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="dbfdd-119"><dt>Pstore.h</dt></span></span> </dl> |



 

 
