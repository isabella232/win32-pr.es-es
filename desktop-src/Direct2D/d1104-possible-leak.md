---
title: D1104 posible fuga
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: El generador se liberó pero la interfaz creada a partir de ella todavía está activa. Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una fuga de memoria.
keywords:
- D1104 posible fuga Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 71ccbee152d60a73fbea5ebac2a1074534b69c3a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104357992"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="b5077-105">D1104: posible fuga</span><span class="sxs-lookup"><span data-stu-id="b5077-105">D1104: Possible Leak</span></span>

<span data-ttu-id="b5077-106">\[  \] Se liberó el generador de fábrica pero la \[ *interfaz* \] de interfaz creada a partir de ella todavía está activa.</span><span class="sxs-lookup"><span data-stu-id="b5077-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="b5077-107">Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="b5077-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="b5077-108">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="b5077-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b5077-109"><span id="factory"></span><span id="FACTORY"></span>*Factory*</span><span class="sxs-lookup"><span data-stu-id="b5077-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="b5077-110">Dirección del generador que se liberó.</span><span class="sxs-lookup"><span data-stu-id="b5077-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="b5077-111"><span id="interface"></span><span id="INTERFACE"></span>*interfaz*</span><span class="sxs-lookup"><span data-stu-id="b5077-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="b5077-112">Dirección de la interfaz que se creó en el *generador*.</span><span class="sxs-lookup"><span data-stu-id="b5077-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

|             |             |
|-------------|-------------|
| <span data-ttu-id="b5077-113">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="b5077-113">Error Level</span></span> | <span data-ttu-id="b5077-114">Información</span><span class="sxs-lookup"><span data-stu-id="b5077-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="b5077-115">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="b5077-115">Possible Causes</span></span>

<span data-ttu-id="b5077-116">El generador se liberó pero la interfaz creada a partir de ella todavía está activa.</span><span class="sxs-lookup"><span data-stu-id="b5077-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




