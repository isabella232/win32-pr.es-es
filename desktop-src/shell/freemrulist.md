---
description: Libera el identificador asociado a la lista de MRU usada más recientemente y escribe los datos almacenados en caché en el registro.
title: Función FreeMRUList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840626"
---
# <a name="freemrulist-function"></a><span data-ttu-id="340f6-103">Función FreeMRUList</span><span class="sxs-lookup"><span data-stu-id="340f6-103">FreeMRUList function</span></span>

<span data-ttu-id="340f6-104">Libera el identificador asociado a la lista de MRU usada más recientemente y escribe los datos almacenados en caché en el registro.</span><span class="sxs-lookup"><span data-stu-id="340f6-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="340f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="340f6-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="340f6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="340f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="340f6-107">*hMRU* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="340f6-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="340f6-108">Tipo: **HANDLE**</span><span class="sxs-lookup"><span data-stu-id="340f6-108">Type: **HANDLE**</span></span>

<span data-ttu-id="340f6-109">Identificador de la lista de MRU que se liberará.</span><span class="sxs-lookup"><span data-stu-id="340f6-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="340f6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="340f6-110">Return value</span></span>

<span data-ttu-id="340f6-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="340f6-111">Type: **int**</span></span>

<span data-ttu-id="340f6-112">Devuelve un valor no negativo si se realiza correctamente; de lo contrario, -1.</span><span class="sxs-lookup"><span data-stu-id="340f6-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="340f6-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="340f6-113">Remarks</span></span>

<span data-ttu-id="340f6-114">Si la lista de MRU se creó con la marca **\_ MRU CACHEWRITE,** llamar a **FreeMRUList** hace que los cambios que aún no se han escrito en la versión de la lista de MRU almacenada en el Registro se escriban en este momento.</span><span class="sxs-lookup"><span data-stu-id="340f6-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="340f6-115">Esta función no se incluye en un encabezado o biblioteca públicos.</span><span class="sxs-lookup"><span data-stu-id="340f6-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="340f6-116">Debe extraerse de comctl32.dll mediante el ordinal 152.</span><span class="sxs-lookup"><span data-stu-id="340f6-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="340f6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="340f6-117">Requirements</span></span>



| <span data-ttu-id="340f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="340f6-118">Requirement</span></span> | <span data-ttu-id="340f6-119">Value</span><span class="sxs-lookup"><span data-stu-id="340f6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="340f6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="340f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="340f6-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="340f6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="340f6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="340f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="340f6-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="340f6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="340f6-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="340f6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="340f6-125"><dt>Comctl32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="340f6-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




