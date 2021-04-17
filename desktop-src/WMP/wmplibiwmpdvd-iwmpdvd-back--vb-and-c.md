---
title: IWMPDVD (método posterior)
description: El método atrás cambia la presentación de un submenú a su menú primario.
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- Back (método) Windows Media Player
- Back (método) Windows Media Player, interfaz IWMPDVD
- Interfaz IWMPDVD Windows Media Player, método back
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661221"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="907df-106">IWMPDVD:: Back (método)</span><span class="sxs-lookup"><span data-stu-id="907df-106">IWMPDVD::back method</span></span>

<span data-ttu-id="907df-107">El método **atrás** cambia la presentación de un submenú a su menú primario.</span><span class="sxs-lookup"><span data-stu-id="907df-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="907df-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="907df-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="907df-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="907df-109">Parameters</span></span>

<span data-ttu-id="907df-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="907df-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="907df-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="907df-111">Return value</span></span>

<span data-ttu-id="907df-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="907df-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="907df-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="907df-113">Remarks</span></span>

<span data-ttu-id="907df-114">Cada DVD se crea de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="907df-114">Every DVD is authored differently.</span></span> <span data-ttu-id="907df-115">Algunos DVDs se crean para que el `back` método esté disponible en el menú raíz, pero cuando se invoca, no hará nada.</span><span class="sxs-lookup"><span data-stu-id="907df-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="907df-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="907df-116">Requirements</span></span>



| <span data-ttu-id="907df-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="907df-117">Requirement</span></span> | <span data-ttu-id="907df-118">Value</span><span class="sxs-lookup"><span data-stu-id="907df-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="907df-119">Versión</span><span class="sxs-lookup"><span data-stu-id="907df-119">Version</span></span><br/>   | <span data-ttu-id="907df-120">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="907df-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="907df-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="907df-121">Namespace</span></span><br/> | <span data-ttu-id="907df-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="907df-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="907df-123">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="907df-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="907df-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="907df-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="907df-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="907df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="907df-126">**Interfaz IWMPDVD (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="907df-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





