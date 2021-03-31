---
title: La funcionalidad de la aplicación de escritorio se ve afectada si no se ejecuta en modo de ventana
description: En Windows 10, las aplicaciones de Windows ya no se muestran en pantalla completa de forma predeterminada; en su lugar, se encuentran en ventanas y las operaciones como la minimización, la restauración, la maximización, el cambio de tamaño (y cualquier otra operación que siempre haya podido realizar en cualquier otra ventana clásica de la aplicación Windows) ahora son posibles.
ms.assetid: 435E85DA-008B-437E-92CB-AC105855760A
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aae44fda5847e5b86616b40ab1bf4ab8cbd206b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418984"
---
# <a name="desktop-app-functionality-is-impacted-if-not-run-in-windowed-mode"></a><span data-ttu-id="be0d5-103">La funcionalidad de la aplicación de escritorio se ve afectada si no se ejecuta en modo de ventana</span><span class="sxs-lookup"><span data-stu-id="be0d5-103">Desktop App functionality is impacted if not run in Windowed Mode</span></span>

<span data-ttu-id="be0d5-104">En Windows 10, las aplicaciones de Windows ya no se muestran en pantalla completa de forma predeterminada; en su lugar, se encuentran en ventanas y las operaciones como la minimización, la restauración, la maximización, el cambio de tamaño (y cualquier otra operación que siempre haya podido realizar en cualquier otra ventana clásica de la aplicación Windows) ahora son posibles.</span><span class="sxs-lookup"><span data-stu-id="be0d5-104">In Windows 10, Windows apps are no longer full-screen by default – instead, they are windowed and operations like minimizing, restoring, maximizing, resizing (and any other operation that you’ve always been able to do to any other Classic Windows application window) is now possible.</span></span>

## <a name="manifestations"></a><span data-ttu-id="be0d5-105">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="be0d5-105">Manifestations</span></span>

<span data-ttu-id="be0d5-106">El cambio más notable ahora es que puede obtener el tamaño de los tamaños arbitrarios que no son solo el tamaño de la pantalla o el alto de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="be0d5-106">The most noticeable change now is that you can get sized to arbitrary sizes that are not just the size of the screen/height of the screen.</span></span> <span data-ttu-id="be0d5-107">Un usuario puede cambiar continuamente el tamaño de la ventana de la aplicación a su gusto (hasta el tamaño mínimo de la ventana de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="be0d5-107">A user can continuously resize the app window to their liking (down to the app’s minimal window size).</span></span> <span data-ttu-id="be0d5-108">Esto es diferente de Windows 8,0 o Windows 8.1, donde el acto de cambiar el tamaño de una ventana era una acción discreta (los usuarios cambiaron el tamaño de una vista en miniatura de la ventana, lo que hacía que la ventana cambiara de tamaño una vez que el usuario confirmó la acción).</span><span class="sxs-lookup"><span data-stu-id="be0d5-108">This is different from Windows 8.0 or Windows 8.1, where the act of resizing a window was a discrete action (users resized a thumbnail of the window, which then caused the window to resize once the user committed the action).</span></span> <span data-ttu-id="be0d5-109">En la actualidad, cuando el usuario arrastra la ventana por la esquina inferior (u otra ubicación del borde), es un cambio de tamaño continuo y la aplicación recibe los mensajes de cambio de tamaño en una fila, en lugar de cambiar el tamaño.</span><span class="sxs-lookup"><span data-stu-id="be0d5-109">Today instead when the user drags the window by the bottom corner (or other border location) it is a continuous resize, and the app receives resize messages in a row, rather than size change.</span></span>

## <a name="mitigations"></a><span data-ttu-id="be0d5-110">Mitigaciones</span><span class="sxs-lookup"><span data-stu-id="be0d5-110">Mitigations</span></span>

<span data-ttu-id="be0d5-111">Para mitigar este riesgo en aplicaciones Windows 8,0 y 8,1:</span><span class="sxs-lookup"><span data-stu-id="be0d5-111">To mitigate this for Windows 8.0 and 8.1 apps:</span></span>

-   <span data-ttu-id="be0d5-112">Si se interrumpe la característica esperada dentro de la funcionalidad de la aplicación, la mitigación del usuario es poner la aplicación en modo de pantalla completa (con el botón "ir a pantalla completa" en la esquina superior derecha de la barra de título).</span><span class="sxs-lookup"><span data-stu-id="be0d5-112">If the expected feature within the app functionality is broken, then the user mitigation is to place the app into full screen mode (by using the “go full screen button” in the upper right corner of the title bar).</span></span>
-   <span data-ttu-id="be0d5-113">Si el inicio de la aplicación se ve afectado porque no se abre según lo esperado, el usuario todavía debe poder cambiar al modo de Tablet PC para forzar que la aplicación se inicie en modo de pantalla completa sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="be0d5-113">If app start-up is impacted that it does not open as expected, then the user should still be able to switch to Tablet Mode to force the app to start in full-screen mode without user intervention.</span></span>

<span data-ttu-id="be0d5-114">La mejor manera de controlarlo es cambiar la aplicación para que tenga en cuenta el hecho de que puede ajustarse a las posiciones y los altos de tamaño sin supervisión (es decir, no tener una tabla codificada de alto y ancho y esperar también las proporciones codificadas de forma rígida).</span><span class="sxs-lookup"><span data-stu-id="be0d5-114">The best way to handle this is to change the app to be aware of the fact that it can be sized to non-monitor sized places/heights (i.e. don’t have a hardcoded table of height/widths and only expect those, or expect hardcoded ratios as well).</span></span> <span data-ttu-id="be0d5-115">Los desarrolladores de aplicaciones deberían esperar que se cambie el tamaño de la aplicación, otro mensaje de cambio de tamaño puede producirse justo después de que se entregue el mensaje de cambio de tamaño actual: como resultado, si la aplicación inicia animaciones durante el cambio de tamaño, es posible que la aplicación reciba otro mensaje de cambio de tamaño justo después (por lo que es importante asegurarse de que este tipo de situación no conduce al bloqueo de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="be0d5-115">App developers should expect that as the app is being resized, that another resizing message can happen right after the current resize message gets delivered – as a result, if the app starts animations during resize, it’s possible that the app may receive another resize message right after (so it’s important to ensure that this type of situation doesn’t lead to the app crashing).</span></span>

 

 




