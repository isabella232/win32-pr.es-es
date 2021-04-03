---
description: El método ShowCursor hace que el cursor esté visible cuando el objeto MSWebDVD está en modo de pantalla completa.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Método ShowCursor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906665"
---
# <a name="showcursor-method"></a><span data-ttu-id="84d8e-103">Método ShowCursor</span><span class="sxs-lookup"><span data-stu-id="84d8e-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="84d8e-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84d8e-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="84d8e-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="84d8e-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="84d8e-106">El `ShowCursor` método hace que el cursor esté visible cuando el objeto **MSWebDVD** está en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="84d8e-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="84d8e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84d8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84d8e-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="84d8e-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="84d8e-109">Especifica si se va a mostrar el cursor como booleano.</span><span class="sxs-lookup"><span data-stu-id="84d8e-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="84d8e-110">Value</span><span class="sxs-lookup"><span data-stu-id="84d8e-110">Value</span></span> | <span data-ttu-id="84d8e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="84d8e-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="84d8e-112">true</span><span class="sxs-lookup"><span data-stu-id="84d8e-112">true</span></span>  | <span data-ttu-id="84d8e-113">Permite mostrar el cursor.</span><span class="sxs-lookup"><span data-stu-id="84d8e-113">Show the cursor</span></span>        |
| <span data-ttu-id="84d8e-114">false</span><span class="sxs-lookup"><span data-stu-id="84d8e-114">false</span></span> | <span data-ttu-id="84d8e-115">No mostrar el cursor</span><span class="sxs-lookup"><span data-stu-id="84d8e-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84d8e-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84d8e-116">Return Value</span></span>

<span data-ttu-id="84d8e-117">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="84d8e-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="84d8e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84d8e-118">Remarks</span></span>

<span data-ttu-id="84d8e-119">Cuando la pantalla del DVD entra en el modo de pantalla completa, el cursor desaparece entre 3 y 5 segundos.</span><span class="sxs-lookup"><span data-stu-id="84d8e-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="84d8e-120">Use este método para hacer que el cursor sea visible de nuevo si los botones de control de la aplicación están visibles en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="84d8e-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



