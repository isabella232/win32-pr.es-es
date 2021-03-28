---
description: Agrega una cadena a la parte superior de la lista de elementos usados más recientemente (MRU).
title: AddMRUStringW función)
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
ms.openlocfilehash: 0d0d65187105f4ad844b349c6ac60b030c464716
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082008"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="d1b92-103">AddMRUStringW función)</span><span class="sxs-lookup"><span data-stu-id="d1b92-103">AddMRUStringW function</span></span>

<span data-ttu-id="d1b92-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d1b92-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="d1b92-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="d1b92-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="d1b92-106">\]</span><span class="sxs-lookup"><span data-stu-id="d1b92-106">\]</span></span>

<span data-ttu-id="d1b92-107">Agrega una cadena a la parte superior de la lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="d1b92-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b92-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1b92-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="d1b92-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1b92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b92-110">*hMRU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1b92-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b92-111">Tipo: **Handle**</span><span class="sxs-lookup"><span data-stu-id="d1b92-111">Type: **HANDLE**</span></span>

<span data-ttu-id="d1b92-112">Identificador de la lista MRU.</span><span class="sxs-lookup"><span data-stu-id="d1b92-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="d1b92-113">*szString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d1b92-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b92-114">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="d1b92-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="d1b92-115">Puntero a los datos.</span><span class="sxs-lookup"><span data-stu-id="d1b92-115">A pointer to the data.</span></span> <span data-ttu-id="d1b92-116">Puede ser una cadena o bien, si la lista MRU se creó con la marca **\_ binaria de MRU** , datos binarios.</span><span class="sxs-lookup"><span data-stu-id="d1b92-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="d1b92-117">En el caso de los datos binarios, el primer **valor DWORD** indica su tamaño.</span><span class="sxs-lookup"><span data-stu-id="d1b92-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b92-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1b92-118">Return value</span></span>

<span data-ttu-id="d1b92-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="d1b92-119">Type: **int**</span></span>

<span data-ttu-id="d1b92-120">Devuelve un valor no negativo si es correcto; de lo contrario,-1.</span><span class="sxs-lookup"><span data-stu-id="d1b92-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b92-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1b92-121">Remarks</span></span>

<span data-ttu-id="d1b92-122">Esta función no está incluida en un encabezado público o una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d1b92-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="d1b92-123">Se puede tener acceso a ella a través de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) o extraer de comctl32.dll por su ordinal, que es 401 para **AddMRUStringW**.</span><span class="sxs-lookup"><span data-stu-id="d1b92-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b92-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1b92-124">Requirements</span></span>



| <span data-ttu-id="d1b92-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b92-125">Requirement</span></span> | <span data-ttu-id="d1b92-126">Value</span><span class="sxs-lookup"><span data-stu-id="d1b92-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b92-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1b92-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b92-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d1b92-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1b92-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1b92-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b92-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d1b92-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1b92-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1b92-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b92-132"><dt>Comctl32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b92-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="d1b92-133">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d1b92-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d1b92-134">**AddMRUStringW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="d1b92-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

