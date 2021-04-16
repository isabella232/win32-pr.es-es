---
description: Cambia el texto de la barra de título de la ventana especificada (si tiene una).
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650127"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="b03c5-103">\_SetWindowText función)</span><span class="sxs-lookup"><span data-stu-id="b03c5-103">\_SetWindowText function</span></span>

<span data-ttu-id="b03c5-104">\[Esta función es un contenedor de la función **SetWindowText** .</span><span class="sxs-lookup"><span data-stu-id="b03c5-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="b03c5-105">Esta función puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="b03c5-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="b03c5-106">Las aplicaciones deben llamar a **SetWindowText** directamente.\]</span><span class="sxs-lookup"><span data-stu-id="b03c5-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="b03c5-107">Cambia el texto de la barra de título de la ventana especificada (si tiene una).</span><span class="sxs-lookup"><span data-stu-id="b03c5-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="b03c5-108">Vea [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span><span class="sxs-lookup"><span data-stu-id="b03c5-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="b03c5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b03c5-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="b03c5-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b03c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b03c5-111">*...*</span><span class="sxs-lookup"><span data-stu-id="b03c5-111">*...*</span></span> 
<span data-ttu-id="b03c5-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b03c5-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b03c5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b03c5-113">Requirements</span></span>



| <span data-ttu-id="b03c5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b03c5-114">Requirement</span></span> | <span data-ttu-id="b03c5-115">Value</span><span class="sxs-lookup"><span data-stu-id="b03c5-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b03c5-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b03c5-116">DLL</span></span><br/> | <dl> <span data-ttu-id="b03c5-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b03c5-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b03c5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b03c5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b03c5-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="b03c5-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
