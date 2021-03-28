---
description: Libera el identificador asociado a la lista de elementos usados más recientemente (MRU) y escribe los datos almacenados en caché en el registro.
title: FreeMRUList función)
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985486"
---
# <a name="freemrulist-function"></a><span data-ttu-id="1a331-103">FreeMRUList función)</span><span class="sxs-lookup"><span data-stu-id="1a331-103">FreeMRUList function</span></span>

<span data-ttu-id="1a331-104">Libera el identificador asociado a la lista de elementos usados más recientemente (MRU) y escribe los datos almacenados en caché en el registro.</span><span class="sxs-lookup"><span data-stu-id="1a331-104">Frees the handle associated with the most recently used (MRU) list and writes cached data to the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a331-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a331-105">Syntax</span></span>


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a><span data-ttu-id="1a331-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a331-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a331-107">*hMRU* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a331-107">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a331-108">Tipo: **Handle**</span><span class="sxs-lookup"><span data-stu-id="1a331-108">Type: **HANDLE**</span></span>

<span data-ttu-id="1a331-109">Identificador de la lista MRU que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="1a331-109">The handle of the MRU list to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a331-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a331-110">Return value</span></span>

<span data-ttu-id="1a331-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="1a331-111">Type: **int**</span></span>

<span data-ttu-id="1a331-112">Devuelve un valor no negativo si es correcto; de lo contrario,-1.</span><span class="sxs-lookup"><span data-stu-id="1a331-112">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a331-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a331-113">Remarks</span></span>

<span data-ttu-id="1a331-114">Si la lista MRU se creó con la **marca \_ CACHEWRITE MRU** , al llamar a **FreeMRUList** , los cambios que todavía no se hayan escrito en la versión de la lista MRU almacenada en el registro se escribirán en este momento.</span><span class="sxs-lookup"><span data-stu-id="1a331-114">If the MRU list was created using the **MRU\_CACHEWRITE** flag, calling **FreeMRUList** causes any changes not yet written to the version of the MRU list stored in registry to be written at this time.</span></span>

<span data-ttu-id="1a331-115">Esta función no está incluida en un encabezado público o una biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1a331-115">This function is not included in a public header or library.</span></span> <span data-ttu-id="1a331-116">Debe extraerse de comctl32.dll por el ordinal 152.</span><span class="sxs-lookup"><span data-stu-id="1a331-116">It must be extracted from comctl32.dll by ordinal 152.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a331-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a331-117">Requirements</span></span>



| <span data-ttu-id="1a331-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a331-118">Requirement</span></span> | <span data-ttu-id="1a331-119">Value</span><span class="sxs-lookup"><span data-stu-id="1a331-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a331-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a331-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1a331-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1a331-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a331-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a331-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1a331-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a331-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1a331-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a331-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a331-125"><dt>Comctl32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1a331-125"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




