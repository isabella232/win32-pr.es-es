---
title: DoReaderMode función)
description: Habilita el modo de lector en una ventana.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- DoReaderMode (función) controles de Windows
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493354"
---
# <a name="doreadermode-function"></a><span data-ttu-id="63e0c-104">DoReaderMode función)</span><span class="sxs-lookup"><span data-stu-id="63e0c-104">DoReaderMode function</span></span>

<span data-ttu-id="63e0c-105">\[**DoReaderMode** está disponible a través de Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="63e0c-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="63e0c-106">Puede que no esté disponible en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="63e0c-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="63e0c-107">Habilita el modo de lector en una ventana.</span><span class="sxs-lookup"><span data-stu-id="63e0c-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e0c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e0c-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="63e0c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63e0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e0c-110">*PRMI* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="63e0c-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63e0c-111">Tipo: **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="63e0c-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="63e0c-112">Puntero a una estructura [**READERMODEINFO**](readermodeinfo.md) que contiene información de inicialización para el modo de lector.</span><span class="sxs-lookup"><span data-stu-id="63e0c-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e0c-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63e0c-113">Return value</span></span>

<span data-ttu-id="63e0c-114">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="63e0c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63e0c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63e0c-115">Remarks</span></span>

<span data-ttu-id="63e0c-116">El modo lector se activa a través de los dispositivos compatibles mediante un clic del mouse, normalmente con un tercer botón del mouse o una rueda de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="63e0c-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="63e0c-117">El movimiento del mouse posterior en un área especificada desplaza el contenido de ese área en lugar de mover un puntero.</span><span class="sxs-lookup"><span data-stu-id="63e0c-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="63e0c-118">Fuera de ese área, se muestra el puntero del mouse y funciona con normalidad.</span><span class="sxs-lookup"><span data-stu-id="63e0c-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="63e0c-119">Un segundo clic del botón o la rueda de desplazamiento libera el dispositivo del modo de lectura.</span><span class="sxs-lookup"><span data-stu-id="63e0c-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="63e0c-120">Esta función no se declara en ningún encabezado público.</span><span class="sxs-lookup"><span data-stu-id="63e0c-120">This function is not declared in any public header.</span></span> <span data-ttu-id="63e0c-121">Para usarlo, debe tener acceso al mismo como ordinal 383 desde Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="63e0c-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="63e0c-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e0c-122">Requirements</span></span>



| <span data-ttu-id="63e0c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e0c-123">Requirement</span></span> | <span data-ttu-id="63e0c-124">Value</span><span class="sxs-lookup"><span data-stu-id="63e0c-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e0c-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e0c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="63e0c-126">Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63e0c-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="63e0c-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63e0c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="63e0c-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="63e0c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="63e0c-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63e0c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e0c-130"><dt>Comctl32.dll (versión 4,72 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="63e0c-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 





