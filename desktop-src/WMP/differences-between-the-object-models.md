---
title: Diferencias entre los modelos de objetos
description: Diferencias entre los modelos de objetos
ms.assetid: a6d2a2d5-2892-461a-aa6d-7e11b504b2af
keywords:
- Media Player de Windows, modelo de objetos
- Modelo de objetos de Windows Media Player, diferencias de versión
- modelo de objetos, diferencias de versión
- Control ActiveX de Windows Media Player, diferencias de versión
- Control ActiveX, diferencias de versión
- Control ActiveX móvil de Windows Media Player, diferencias de versión
- Windows Media Player Mobile, modelo de objetos
- Guía de migración, diferencias de versión
- versiones de Windows Media Player, modelo de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a5341067e2daad0f44fbdd7075f0f543bac2fd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695398"
---
# <a name="differences-between-the-object-models"></a><span data-ttu-id="a3fb0-112">Diferencias entre los modelos de objetos</span><span class="sxs-lookup"><span data-stu-id="a3fb0-112">Differences Between the Object Models</span></span>

<span data-ttu-id="a3fb0-113">Hay dos diferencias principales entre el modelo de objetos de Windows Media Player 6,4 y el modelo de objetos de Windows Media Player 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-113">There are two primary differences between the Windows Media Player 6.4 object model and the Windows Media Player 7 or later object model.</span></span>

-   <span data-ttu-id="a3fb0-114">**CLSID** de El modelo de objetos de Windows Media Player 7 o posterior es una salida completa del modelo de objetos de la versión 6,4.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-114">**CLSID** The Windows Media Player 7 or later object model is a complete departure from the version 6.4 object model.</span></span> <span data-ttu-id="a3fb0-115">La especificación del modelo de objetos componentes (COM) requiere que todas las interfaces existentes sigan funcionando en las nuevas versiones de un componente COM.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-115">The Component Object Model (COM) specification requires that all existing interfaces must continue to function in new versions of a COM component.</span></span> <span data-ttu-id="a3fb0-116">Esto significa que se pueden agregar nuevas interfaces a un componente COM, pero las interfaces existentes no deben modificarse nunca, lo que garantiza que el código de cliente anterior funcionará siempre con el componente determinado que se diseñó para usar.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-116">This means that new interfaces can be added to a COM component, but existing interfaces must never be altered, ensuring older client code will always work with the particular component it was designed to use.</span></span> <span data-ttu-id="a3fb0-117">Por lo tanto, el control ActiveX Windows Media Player 7 o versiones posteriores tiene un nuevo identificador de clase: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-117">Therefore, the Windows Media Player 7 or later ActiveX control has a new class ID: 6BF52A52-394A-11D3-B153-00C04F79FAA6.</span></span> <span data-ttu-id="a3fb0-118">Si desea aprovechar las ventajas de la nueva funcionalidad del control para esta versión, debe cambiar el CLSID.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-118">If you want to take advantage of the new functionality of the control for this version, you must change your CLSID.</span></span>
-   <span data-ttu-id="a3fb0-119">**Modelo de objetos jerárquicos** Si ha usado el control ActiveX de Windows Media Player 6,4, es posible que haya observado que se tiene acceso a todas las propiedades, métodos y eventos a través del mismo objeto: el objeto **Player** .</span><span class="sxs-lookup"><span data-stu-id="a3fb0-119">**Hierarchical Object Model** If you've been using the Windows Media Player 6.4 ActiveX control, you may have noticed that all the properties, methods, and events are accessed through the same object: the **Player** object.</span></span> <span data-ttu-id="a3fb0-120">Por el contrario, el modelo de objetos de Windows Media Player 7 o posterior se organiza como una jerarquía de objetos.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-120">By contrast, the Windows Media Player 7 or later object model is organized as a hierarchy of objects.</span></span> <span data-ttu-id="a3fb0-121">El objeto **Player** sigue siendo el objeto raíz, pero ahora se tiene acceso a las funciones a través de diversos objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="a3fb0-121">The **Player** object is still the root object, but functions are now accessed through a variety of child objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3fb0-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3fb0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3fb0-123">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="a3fb0-123">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




