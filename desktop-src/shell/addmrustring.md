---
description: Agrega una cadena a la parte superior de la lista usada más recientemente (MRU).
title: Función AddMRUStringW
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841196"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="6f1a4-103">Función AddMRUStringW</span><span class="sxs-lookup"><span data-stu-id="6f1a4-103">AddMRUStringW function</span></span>

<span data-ttu-id="6f1a4-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="6f1a4-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="6f1a4-106">\]</span><span class="sxs-lookup"><span data-stu-id="6f1a4-106">\]</span></span>

<span data-ttu-id="6f1a4-107">Agrega una cadena a la parte superior de la lista de mru usada más recientemente.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1a4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f1a4-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="6f1a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f1a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f1a4-110">*hMRU* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6f1a4-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1a4-111">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="6f1a4-111">Type: **HANDLE**</span></span>

<span data-ttu-id="6f1a4-112">Identificador de la lista de MRU.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="6f1a4-113">*szString* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="6f1a4-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f1a4-114">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6f1a4-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6f1a4-115">Puntero a los datos.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-115">A pointer to the data.</span></span> <span data-ttu-id="6f1a4-116">Puede ser una cadena o, si se creó la lista de MRU con la **marca \_ BINARY de MRU,** datos binarios.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="6f1a4-117">En el caso de los datos binarios, el primer **DWORD** indica su tamaño.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f1a4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f1a4-118">Return value</span></span>

<span data-ttu-id="6f1a4-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6f1a4-119">Type: **int**</span></span>

<span data-ttu-id="6f1a4-120">Devuelve un valor no negativo si se realiza correctamente; de lo contrario, -1.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f1a4-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f1a4-121">Remarks</span></span>

<span data-ttu-id="6f1a4-122">Esta función no se incluye en un encabezado o biblioteca públicos.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="6f1a4-123">Se puede acceder a él a través de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraerse de comctl32.dll por su ordinal, que es 401 **para AddMRUStringW**.</span><span class="sxs-lookup"><span data-stu-id="6f1a4-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1a4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f1a4-124">Requirements</span></span>



| <span data-ttu-id="6f1a4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f1a4-125">Requirement</span></span> | <span data-ttu-id="6f1a4-126">Value</span><span class="sxs-lookup"><span data-stu-id="6f1a4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1a4-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f1a4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1a4-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f1a4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6f1a4-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f1a4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1a4-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f1a4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6f1a4-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f1a4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f1a4-132"><dt>Comctl32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6f1a4-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="6f1a4-133">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="6f1a4-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6f1a4-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="6f1a4-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

