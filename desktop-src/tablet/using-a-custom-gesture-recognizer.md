---
description: Puede usar un reconocedor de gestos personalizado de forma independiente o además de GestureRecognizer. cree el reconocedor de gestos personalizado como IStylusSyncPlugin, haga que cree CustomStylusData e incluya el complemento en el mismo StylusSyncPluginCollection que el GestureRecognizer. En IStylusSyncPlugin, combine las notificaciones de gestos de ambos reconocedores en las notificaciones para que las consuma una aplicación.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Usar un reconocedor de gestos personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705547"
---
# <a name="using-a-custom-gesture-recognizer"></a><span data-ttu-id="d93c4-104">Usar un reconocedor de gestos personalizado</span><span class="sxs-lookup"><span data-stu-id="d93c4-104">Using a Custom Gesture Recognizer</span></span>

<span data-ttu-id="d93c4-105">Puede usar un reconocedor de gestos personalizado de forma independiente o además de [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="d93c4-105">You can use a custom gesture recognizer independently, or in addition to the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span>

<span data-ttu-id="d93c4-106">Cree el reconocedor de gestos personalizado como un [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), haga que cree [CustomStylusData](/previous-versions/ms575208(v=vs.100))e incluya el complemento en el mismo [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) que [**GestureRecognizer**](gesturerecognizer-class.md).</span><span class="sxs-lookup"><span data-stu-id="d93c4-106">Create your custom gesture recognizer as an [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), have it create [CustomStylusData](/previous-versions/ms575208(v=vs.100)), and include the plug-in in the same [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) as the [**GestureRecognizer**](gesturerecognizer-class.md).</span></span> <span data-ttu-id="d93c4-107">En **IStylusSyncPlugin**, combine las notificaciones de gestos de ambos reconocedores en las notificaciones para que las consuma una aplicación.</span><span class="sxs-lookup"><span data-stu-id="d93c4-107">In the **IStylusSyncPlugin**, combine gesture notifications from both recognizers into notifications to be consumed by an application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d93c4-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d93c4-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d93c4-109">Acceso y manipulación de la entrada del lápiz óptico</span><span class="sxs-lookup"><span data-stu-id="d93c4-109">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
