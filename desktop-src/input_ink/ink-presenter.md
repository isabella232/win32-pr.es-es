---
description: Las API de moderador de lápiz permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de entrada de lápiz (estándar o modificada) a través de un objeto InkPresenter insertado en el árbol visual DirectComposition de la aplicación.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Presentador de tinta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 9bd9f4c3c98b443110a0a7948075ab836a9493c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277844"
---
# <a name="ink-presenter"></a><span data-ttu-id="9fbe4-103">Presentador de tinta</span><span class="sxs-lookup"><span data-stu-id="9fbe4-103">Ink presenter</span></span>

<span data-ttu-id="9fbe4-104">Las API del presentador de tinta permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de entradas manuscritas (estándar y modificado) a través de un objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) insertado en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-104">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span>

> [!Note]
>
> <span data-ttu-id="9fbe4-105">La entrada de lápiz estándar (sugerencia o botón de la punta del lápiz o del borrador) no se modifica con una prestación secundaria, como un botón de barril del lápiz, un botón secundario del mouse o similar.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-105">Standard ink input (pen tip or eraser tip/button) is not modified with a secondary affordance, such as a pen barrel button, right mouse button, or similar.</span></span>

<span data-ttu-id="9fbe4-106">Las aplicaciones Plataforma universal de Windows (UWP) que usan lenguaje XAML (XAML) proporcionan esta funcionalidad a través de un control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) junto con un objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) que se conecta al árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de XAML.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-106">Universal Windows Platform (UWP) apps using Extensible Application Markup Language (XAML) provide this functionality through an [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control along with an [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) object that connects to the XAML [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span> <span data-ttu-id="9fbe4-107">Para obtener más información, consulte [interacciones de lápiz y](/windows/uwp/design/input/pen-and-stylus-interactions)lápiz.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-107">For more detail, see [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions).</span></span>

<span data-ttu-id="9fbe4-108">El [representador de tinta](ink-renderer.md) está diseñado para que lo usen los desarrolladores de aplicaciones universales de Windows interesados en proporcionar la funcionalidad de InkPresenter de [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)basada en XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) en aplicaciones Win32 nativas.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-108">[Ink renderer](ink-renderer.md) is designed for use by Universal Windows app developers interested in providing XAML-based [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)/[**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) functionality in native Win32 apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fbe4-109">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9fbe4-109">In this section</span></span>



| <span data-ttu-id="9fbe4-110">Tema</span><span class="sxs-lookup"><span data-stu-id="9fbe4-110">Topic</span></span>                                                               | <span data-ttu-id="9fbe4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fbe4-111">Description</span></span>                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fbe4-112">Clases de presentador de tinta</span><span class="sxs-lookup"><span data-stu-id="9fbe4-112">Ink presenter classes</span></span>](ink-presenter-classes.md)<br/>       | <span data-ttu-id="9fbe4-113">Los temas contenidos en esta sección proporcionan las especificaciones de referencia para las clases de presentador de tinta.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-113">The topics contained in this section provide the reference specifications for Ink presenter classes.</span></span> <br/>    |
| [<span data-ttu-id="9fbe4-114">Interfaces de presentador de tinta</span><span class="sxs-lookup"><span data-stu-id="9fbe4-114">Ink presenter interfaces</span></span>](ink-presenter-interfaces.md)<br/> | <span data-ttu-id="9fbe4-115">Los temas contenidos en esta sección proporcionan las especificaciones de referencia de las interfaces de presentación de tinta.</span><span class="sxs-lookup"><span data-stu-id="9fbe4-115">The topics contained in this section provide the reference specifications for Ink presenter interfaces.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="9fbe4-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9fbe4-116">Related topics</span></span>

<span data-ttu-id="9fbe4-117">[Presentador de tinta](ink-presenter.md), [interacciones de lápiz y lápiz óptico](/windows/uwp/design/input/pen-and-stylus-interactions), ejemplo de análisis de [tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de entrada de lápiz [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="9fbe4-117">[Ink presenter](ink-presenter.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
