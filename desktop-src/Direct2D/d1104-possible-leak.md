---
title: D1104 Posible pérdida
ms.assetid: 564de2e2-5004-43e8-8616-1ab11127738a
description: Se lanzó el generador, pero la interfaz creada a partir de ella sigue estando activo. Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una pérdida de memoria.
keywords:
- D1104 Possible Leak Direct2D
topic_type:
- apiref
api_name:
- D1104 Possible Leak
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: b6629a0da2b89e13feebc33fe5742e3459fc082b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548680"
---
# <a name="d1104-possible-leak"></a><span data-ttu-id="63e5f-105">D1104: posible pérdida</span><span class="sxs-lookup"><span data-stu-id="63e5f-105">D1104: Possible Leak</span></span>

<span data-ttu-id="63e5f-106">Se lanzó \[ *el generador* \] de fábrica, pero la interfaz \[ *creada* a partir de ella \] sigue estando activo.</span><span class="sxs-lookup"><span data-stu-id="63e5f-106">The factory \[*factory*\] was released but the interface \[*interface*\] created from it is still alive.</span></span> <span data-ttu-id="63e5f-107">Aunque es válido liberar recursos después de liberar el generador, esta condición podría indicar una pérdida de memoria.</span><span class="sxs-lookup"><span data-stu-id="63e5f-107">While it is valid to release resources after releasing the factory, this condition could be indicative of a memory leak.</span></span>

## <a name="placeholders"></a><span data-ttu-id="63e5f-108">Marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="63e5f-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="63e5f-109"><span id="factory"></span><span id="FACTORY"></span>*Fábrica*</span><span class="sxs-lookup"><span data-stu-id="63e5f-109"><span id="factory"></span><span id="FACTORY"></span>*factory*</span></span>
</dt> <dd>

<span data-ttu-id="63e5f-110">Dirección del generador que se publicó.</span><span class="sxs-lookup"><span data-stu-id="63e5f-110">The address of the factory that was released.</span></span>

</dd> <dt>

<span data-ttu-id="63e5f-111"><span id="interface"></span><span id="INTERFACE"></span>*Interfaz*</span><span class="sxs-lookup"><span data-stu-id="63e5f-111"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="63e5f-112">Dirección de la interfaz que se creó en el *generador*.</span><span class="sxs-lookup"><span data-stu-id="63e5f-112">The address of the interface that was created on the *factory*.</span></span>

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| <span data-ttu-id="63e5f-113">Nivel de error</span><span class="sxs-lookup"><span data-stu-id="63e5f-113">Error Level</span></span> | <span data-ttu-id="63e5f-114">Information</span><span class="sxs-lookup"><span data-stu-id="63e5f-114">Information</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="63e5f-115">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="63e5f-115">Possible Causes</span></span>

<span data-ttu-id="63e5f-116">Se lanzó el generador, pero la interfaz creada a partir de ella sigue estando activo.</span><span class="sxs-lookup"><span data-stu-id="63e5f-116">The factory was released but the interface created from it is still alive.</span></span>

 

 




