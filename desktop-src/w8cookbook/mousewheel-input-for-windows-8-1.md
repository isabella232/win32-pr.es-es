---
title: Entrada MouseWheel para Windows 8.1
description: Entrada MouseWheel para Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903307"
---
# <a name="mousewheel-input-for-windows-81"></a><span data-ttu-id="c94ff-103">Entrada MouseWheel para Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c94ff-103">Mousewheel input for Windows 8.1</span></span>

## <a name="platform"></a><span data-ttu-id="c94ff-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="c94ff-104">Platform</span></span>

<dl> <span data-ttu-id="c94ff-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c94ff-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="c94ff-106">Servidores: Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c94ff-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="c94ff-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c94ff-107">Description</span></span>

<span data-ttu-id="c94ff-108">En Windows 8.1, los eventos MouseWheel ya no se entregan en función del foco del teclado como en versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="c94ff-108">In Windows 8.1, mousewheel events are no longer delivered based on keyboard focus as in previous versions of Windows.</span></span> <span data-ttu-id="c94ff-109">En Windows 8.1, si se mantiene el mouse sobre una aplicación de la tienda, se entregará MouseWheel a esa aplicación; por motivos de compatibilidad, sin embargo, si el mouse se mantiene sobre una aplicación de escritorio, MouseWheel se seguirá entregando en función del foco del teclado.</span><span class="sxs-lookup"><span data-stu-id="c94ff-109">In Windows 8.1, if the mouse is hovering over a store app, mousewheel will be delivered to that app; for compatibility purposes, however, if the mouse is hovering over a desktop app, mousewheel will continue to be delivered based on keyboard focus.</span></span>

## <a name="manifestations"></a><span data-ttu-id="c94ff-110">Manifestaciones</span><span class="sxs-lookup"><span data-stu-id="c94ff-110">Manifestations</span></span>

<span data-ttu-id="c94ff-111">Cuando el mouse se mantiene sobre las aplicaciones de la tienda, MouseWheel desplazará cualquier contenido aplicable sin que el usuario tenga que hacer clic en la aplicación de la tienda.</span><span class="sxs-lookup"><span data-stu-id="c94ff-111">When the mouse is hovering over Store apps, mousewheel will scroll any applicable content without the user having to click on the Store app.</span></span> <span data-ttu-id="c94ff-112">Esto también se aplica a la pantalla Inicio.</span><span class="sxs-lookup"><span data-stu-id="c94ff-112">This also applies to the start screen.</span></span> <span data-ttu-id="c94ff-113">Esto hace que el desplazamiento por MouseWheel sea una interacción más sencilla en Windows 8.1 que en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c94ff-113">This makes scrolling by mousewheel a simpler interaction in Windows 8.1 than in Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="c94ff-114">Mitigación</span><span class="sxs-lookup"><span data-stu-id="c94ff-114">Mitigation</span></span>

<span data-ttu-id="c94ff-115">En su mayor parte, este cambio no debe tener ningún impacto en las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="c94ff-115">For the most part this change should have no impact on existing apps.</span></span> <span data-ttu-id="c94ff-116">Si una aplicación de la tienda escucha eventos MouseWheel solo después de haber registrado un evento de clic del mouse, esa aplicación no podría responder a MouseWheel hasta que el usuario haga clic activamente en ella.</span><span class="sxs-lookup"><span data-stu-id="c94ff-116">If a Store app listened for mousewheel events only after it has registered a mouse click event, that app would not be likely to respond to mousewheel until the user actively clicked it.</span></span> <span data-ttu-id="c94ff-117">Por lo tanto, la desventaja más probable es que una aplicación continúe funcionando igual que en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c94ff-117">Consequently, the most likely downside here is simply that an app continues to operate just as it did in Windows 8.</span></span> <span data-ttu-id="c94ff-118">En el caso de las aplicaciones de escritorio, tener el foco de teclado ya no proporciona a la aplicación un monopolio sobre la entrada MouseWheel, pero tampoco se rompe de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="c94ff-118">For desktop apps, having keyboard focus no longer gives the app a monopoly over mousewheel input, but this also does not in any way break those apps.</span></span> <span data-ttu-id="c94ff-119">Por tanto, no se requieren mitigaciones a corto plazo.</span><span class="sxs-lookup"><span data-stu-id="c94ff-119">So no short-term mitigations are required.</span></span>

## <a name="solution"></a><span data-ttu-id="c94ff-120">Solución</span><span class="sxs-lookup"><span data-stu-id="c94ff-120">Solution</span></span>

<span data-ttu-id="c94ff-121">Los desarrolladores de aplicaciones de la tienda deberían esperar recibir eventos MouseWheel sin un evento de clic del mouse precursor.</span><span class="sxs-lookup"><span data-stu-id="c94ff-121">Store app developers should expect to receive mousewheel events without a precursor mouse click event.</span></span> <span data-ttu-id="c94ff-122">Por ejemplo, no deberían escuchar los eventos MouseWheel solo después de registrar un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="c94ff-122">They should not, for example, listen for mousewheel events only after registering a mouse click.</span></span> <span data-ttu-id="c94ff-123">Del mismo modo, las aplicaciones de escritorio no deben intentar capturar eventos MouseWheel (por ejemplo, estableciendo un enlace de bajo nivel) cuando tienen el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="c94ff-123">Similarly, desktop applications should not try to capture mousewheel events (for example, by setting a low-level hook) when they have keyboard focus.</span></span>

## <a name="tests"></a><span data-ttu-id="c94ff-124">Pruebas</span><span class="sxs-lookup"><span data-stu-id="c94ff-124">Tests</span></span>

<span data-ttu-id="c94ff-125">Los desarrolladores de aplicaciones de la tienda deben probar Windows 8.1 para comprobar que todas las funciones de desplazamiento funcionan siempre que se mantiene el mouse sobre la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c94ff-125">Store app developers should test on Windows 8.1 to verify that all scrolling functionality works whenever the mouse is hovering over the app.</span></span> <span data-ttu-id="c94ff-126">Los desarrolladores de aplicaciones de escritorio deben probar Windows 8.1 para comprobar que no capturan eventos MouseWheel (según las instrucciones anteriores).</span><span class="sxs-lookup"><span data-stu-id="c94ff-126">Desktop app developers should test on Windows 8.1 to verify that they are not capturing mousewheel events (per guidance above.)</span></span>

 

 




