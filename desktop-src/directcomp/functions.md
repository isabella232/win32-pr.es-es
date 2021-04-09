---
title: Funciones de DirectComposition
description: En esta sección se describen las funciones proporcionadas por Microsoft DirectComposition \ 32; API.
ms.assetid: 750FDFD5-ADD5-43B3-A596-ECDB82C2EF73
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934e0b7e32f22faaefdf625e0af2a42a03e469d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149361"
---
# <a name="directcomposition-functions"></a><span data-ttu-id="f96d2-103">Funciones de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="f96d2-103">DirectComposition functions</span></span>

<span data-ttu-id="f96d2-104">En esta sección se describen las funciones que proporciona la API de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="f96d2-104">This section describes the functions provided by the Microsoft DirectComposition API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f96d2-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="f96d2-105">In this section</span></span>



| <span data-ttu-id="f96d2-106">Tema</span><span class="sxs-lookup"><span data-stu-id="f96d2-106">Topic</span></span>                                                                                       | <span data-ttu-id="f96d2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f96d2-107">Description</span></span>                                                                                                                                          |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f96d2-108">**DCompositionAttachMouseDragToHwnd**</span><span class="sxs-lookup"><span data-stu-id="f96d2-108">**DCompositionAttachMouseDragToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousedragtohwnd)<br/>   | <span data-ttu-id="f96d2-109">Crea una interacción/InputSink para enrutar el botón del mouse hacia abajo y los eventos de movimiento y posterior posteriores al HWND especificado.</span><span class="sxs-lookup"><span data-stu-id="f96d2-109">Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.</span></span><br/>                      |
| [<span data-ttu-id="f96d2-110">**DCompositionAttachMouseWheelToHwnd**</span><span class="sxs-lookup"><span data-stu-id="f96d2-110">**DCompositionAttachMouseWheelToHwnd**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositionattachmousewheeltohwnd)<br/> | <span data-ttu-id="f96d2-111">Crea una interacción/InputSink para enrutar los mensajes de la rueda del mouse al HWND especificado.</span><span class="sxs-lookup"><span data-stu-id="f96d2-111">Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.</span></span> <br/>                                                        |
| [<span data-ttu-id="f96d2-112">**DCompositionCreateDevice**</span><span class="sxs-lookup"><span data-stu-id="f96d2-112">**DCompositionCreateDevice**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice)<br/>                     | <span data-ttu-id="f96d2-113">Crea un nuevo objeto de dispositivo que se puede usar para crear otros objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="f96d2-113">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="f96d2-114">**DCompositionCreateDevice2**</span><span class="sxs-lookup"><span data-stu-id="f96d2-114">**DCompositionCreateDevice2**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatedevice2)<br/>                   | <span data-ttu-id="f96d2-115">Crea un nuevo objeto de dispositivo que se puede usar para crear otros objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="f96d2-115">Creates a new device object that can be used to create other DirectComposition objects.</span></span><br/>                                                   |
| [<span data-ttu-id="f96d2-116">**DCompositionCreateDevice3**</span><span class="sxs-lookup"><span data-stu-id="f96d2-116">**DCompositionCreateDevice3**</span></span>](/windows/desktop/api/dcomp/nf-dcomp-dcompositioncreatedevice3)<br/>                   | <span data-ttu-id="f96d2-117">Crea un nuevo objeto de dispositivo DirectComposition, que se puede usar para crear otros objetos DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="f96d2-117">Creates a new DirectComposition device object, which can be used to create other DirectComposition objects.</span></span><br/>                               |
| [<span data-ttu-id="f96d2-118">**DCompositionCreateSurfaceHandle**</span><span class="sxs-lookup"><span data-stu-id="f96d2-118">**DCompositionCreateSurfaceHandle**</span></span>](/windows/desktop/api/Dcomp/nf-dcomp-dcompositioncreatesurfacehandle)<br/>       | <span data-ttu-id="f96d2-119">Crea un nuevo objeto de superficie de composición que se puede enlazar a una cadena de intercambio de Microsoft DirectX o a un búfer de intercambio y que está asociado a un objeto visual.</span><span class="sxs-lookup"><span data-stu-id="f96d2-119">Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.</span></span><br/> |
| <span data-ttu-id="f96d2-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f96d2-120">[**DCompositionGetFrameStatistics**](/previous-versions/windows/desktop/legacy/mt589902(v=vs.85))</span></span><br/>         | <span data-ttu-id="f96d2-121">Recupera información de estadísticas de composición.</span><span class="sxs-lookup"><span data-stu-id="f96d2-121">Retrieves composition statistics information.</span></span><br/>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="f96d2-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f96d2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f96d2-123">Referencia de DirectComposition</span><span class="sxs-lookup"><span data-stu-id="f96d2-123">DirectComposition Reference</span></span>](reference.md)
</dt> </dl>

 

