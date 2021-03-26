---
UID: ''
title: SHIsChildOrSelf función)
description: Compara si una ventana es igual a, un elemento secundario de, o un descendiente de, una segunda ventana.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: IsChild
ms.topic: reference
req.header: Shlwapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- api-ms-win-shlwapi-winrt-storage-l1-1-1.dll
api_name:
- SHIsChildOrSelf
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 911bb0b2a544197ca6db761e05adac79e97c3f69
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "104997020"
---
# <a name="shischildorself-function"></a><span data-ttu-id="d6a11-103">SHIsChildOrSelf función)</span><span class="sxs-lookup"><span data-stu-id="d6a11-103">SHIsChildOrSelf function</span></span>

## <a name="description"></a><span data-ttu-id="d6a11-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6a11-104">Description</span></span>

<span data-ttu-id="d6a11-105">\[Esta función está disponible a través de Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d6a11-105">\[This function is available through Windows XP and Windows Server 2003.</span></span>
<span data-ttu-id="d6a11-106">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6a11-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d6a11-107">Compara si una ventana es igual a, un elemento secundario de, o un descendiente de, una segunda ventana.</span><span class="sxs-lookup"><span data-stu-id="d6a11-107">Compares whether a window is equal to, a child of, or a descendant of, a second window.</span></span>

```cpp
HRESULT SHIsChildOrSelf(
  _In_ HWND hwndParent,
  _In_ HWND hwnd
);
```

## <a name="parameters"></a><span data-ttu-id="d6a11-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d6a11-108">Parameters</span></span>

### <a name="hwndparent-in"></a><span data-ttu-id="d6a11-109">hwndParent [in]</span><span class="sxs-lookup"><span data-stu-id="d6a11-109">hwndParent [in]</span></span>

<span data-ttu-id="d6a11-110">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="d6a11-110">Type: **HWND**</span></span>

<span data-ttu-id="d6a11-111">Identificador de la primera ventana.</span><span class="sxs-lookup"><span data-stu-id="d6a11-111">A handle to the first window.</span></span>

### <a name="hwnd-in"></a><span data-ttu-id="d6a11-112">HWND [in]</span><span class="sxs-lookup"><span data-stu-id="d6a11-112">hwnd [in]</span></span>

<span data-ttu-id="d6a11-113">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="d6a11-113">Type: **HWND**</span></span>

<span data-ttu-id="d6a11-114">Identificador de una ventana que se va a probar con *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="d6a11-114">A handle to a window to be tested against *hwndParent*.</span></span>

## <a name="returns"></a><span data-ttu-id="d6a11-115">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="d6a11-115">Returns</span></span>

<span data-ttu-id="d6a11-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d6a11-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d6a11-117">Devuelve **S_OK** si la ventana especificada por *hWnd* es igual a, un elemento secundario de o un descendiente de la ventana especificada por *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="d6a11-117">Returns **S_OK** if the window specified by *hwnd* is equal to, a child of, or a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="d6a11-118">Devuelve **S_FALSE** si la ventana especificada por HWND no es igual a, no es un elemento secundario de, y no es un descendiente de la ventana especificada por *hwndParent*.</span><span class="sxs-lookup"><span data-stu-id="d6a11-118">Returns **S_FALSE** if the window specified by hwnd is not equal to, not a child of, and not a descendent of the window specified by *hwndParent*.</span></span>
<span data-ttu-id="d6a11-119">El valor devuelto es indefinido si alguno de los identificadores de ventana no es válido.</span><span class="sxs-lookup"><span data-stu-id="d6a11-119">The return value is undefined if either window handle is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6a11-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6a11-120">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="d6a11-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6a11-121">See also</span></span>

[<span data-ttu-id="d6a11-122">Ischild (</span><span class="sxs-lookup"><span data-stu-id="d6a11-122">IsChild</span></span>](/windows/desktop/api/winuser/nf-winuser-ischild)
