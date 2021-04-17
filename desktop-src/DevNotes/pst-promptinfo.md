---
description: Define el comportamiento de la solicitud del almacén protegido cada vez que muestra una interfaz de usuario.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: PST_PROMPTINFO estructura (pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670839"
---
# <a name="pst_promptinfo-structure"></a><span data-ttu-id="1701b-103">\_Estructura PROMPTINFO de PST</span><span class="sxs-lookup"><span data-stu-id="1701b-103">PST\_PROMPTINFO structure</span></span>

<span data-ttu-id="1701b-104">\[El almacenamiento protegido (pstore) está disponible para su uso en Windows Server 2003 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1701b-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="1701b-105">Solo está disponible para las operaciones de solo lectura en Windows Server 2008 y Windows Vista, pero puede no estar disponible en las versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="1701b-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="1701b-106">Pstore usa una implementación anterior de la protección de datos.</span><span class="sxs-lookup"><span data-stu-id="1701b-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="1701b-107">Se recomienda encarecidamente a los desarrolladores que aprovechen la protección de datos más segura proporcionada por las funciones [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="1701b-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="1701b-108">Define el comportamiento de la solicitud del almacén protegido cada vez que muestra una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1701b-108">Defines the prompting behavior of the Protected Store whenever it displays a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="1701b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1701b-109">Syntax</span></span>


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a><span data-ttu-id="1701b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1701b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1701b-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="1701b-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="1701b-112">Tamaño de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="1701b-112">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1701b-113">**dwPromptFlags**</span><span class="sxs-lookup"><span data-stu-id="1701b-113">**dwPromptFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1701b-114">Esta marca se omite.</span><span class="sxs-lookup"><span data-stu-id="1701b-114">This flag is ignored.</span></span>



| <span data-ttu-id="1701b-115">Value</span><span class="sxs-lookup"><span data-stu-id="1701b-115">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="1701b-116">Significado</span><span class="sxs-lookup"><span data-stu-id="1701b-116">Meaning</span></span>                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <span data-ttu-id="1701b-117"><dt>**Archivo pst \_ PF \_ siempre \_ muestra**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1701b-117"><dt>**PST\_PF\_ALWAYS\_SHOW**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="1701b-118">Solicita que el proveedor muestre el cuadro de diálogo de solicitud al usuario, incluso si no es necesario para este acceso.</span><span class="sxs-lookup"><span data-stu-id="1701b-118">Requests that the provider show the prompt dialog to the user even if it is not required for this access.</span></span> <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <span data-ttu-id="1701b-119"><dt>**Archivo pst \_ PF \_ nunca \_ muestra**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1701b-119"><dt>**PST\_PF\_NEVER\_SHOW**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="1701b-120">No muestre el cuadro de diálogo de solicitud al usuario.</span><span class="sxs-lookup"><span data-stu-id="1701b-120">Do not show the prompt dialog to the user.</span></span><br/>                                                                 |



 

</dd> <dt>

<span data-ttu-id="1701b-121">**hwndApp**</span><span class="sxs-lookup"><span data-stu-id="1701b-121">**hwndApp**</span></span>
</dt> <dd>

<span data-ttu-id="1701b-122">Identificador de la ventana primaria de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1701b-122">The handle to the parent window for the user interface.</span></span> <span data-ttu-id="1701b-123">El miembro **hwndApp** determina dónde aparece la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1701b-123">The **hwndApp** member determines where the user interface appears.</span></span> <span data-ttu-id="1701b-124">Si se pasa **null** , se considera que el escritorio es la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="1701b-124">If **NULL** is passed, the desktop is considered to be the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="1701b-125">**szPrompt**</span><span class="sxs-lookup"><span data-stu-id="1701b-125">**szPrompt**</span></span>
</dt> <dd>

<span data-ttu-id="1701b-126">La cadena de solicitud.</span><span class="sxs-lookup"><span data-stu-id="1701b-126">The prompt string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1701b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1701b-127">Requirements</span></span>



| <span data-ttu-id="1701b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1701b-128">Requirement</span></span> | <span data-ttu-id="1701b-129">Value</span><span class="sxs-lookup"><span data-stu-id="1701b-129">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1701b-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1701b-130">Header</span></span><br/> | <dl> <span data-ttu-id="1701b-131"><dt>Pstore. h</dt></span><span class="sxs-lookup"><span data-stu-id="1701b-131"><dt>Pstore.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1701b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1701b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1701b-133">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="1701b-133">**DeleteItem**</span></span>](ipstore-deleteitem.md)
</dt> <dt>

[<span data-ttu-id="1701b-134">**OpenItem**</span><span class="sxs-lookup"><span data-stu-id="1701b-134">**OpenItem**</span></span>](ipstore-openitem.md)
</dt> <dt>

[<span data-ttu-id="1701b-135">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="1701b-135">**ReadItem**</span></span>](ipstore-readitem.md)
</dt> <dt>

[<span data-ttu-id="1701b-136">**WriteItem**</span><span class="sxs-lookup"><span data-stu-id="1701b-136">**WriteItem**</span></span>](ipstore-writeitem.md)
</dt> </dl>

 

 
