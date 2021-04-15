---
description: Obtenga información sobre las distintas API de entrada manuscrita de escritorio para aplicaciones Windows.
ms.assetid: 0691afb1-575a-4bb7-8fa5-006b231b8f1f
title: Entrada manuscrita
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ffb67d452e3bee327195f8ff920bfcab3c0232a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720624"
---
# <a name="ink-input"></a><span data-ttu-id="4b914-103">Entrada manuscrita</span><span class="sxs-lookup"><span data-stu-id="4b914-103">Ink input</span></span>

<span data-ttu-id="4b914-104">Obtenga información sobre las distintas API de entrada manuscrita de escritorio para aplicaciones Windows.</span><span class="sxs-lookup"><span data-stu-id="4b914-104">Learn about the various Desktop inking APIs for Windows apps.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4b914-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="4b914-105">In this section</span></span>

| <span data-ttu-id="4b914-106">Tema</span><span class="sxs-lookup"><span data-stu-id="4b914-106">Topic</span></span> | <span data-ttu-id="4b914-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b914-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="4b914-108">Presentador de tinta</span><span class="sxs-lookup"><span data-stu-id="4b914-108">Ink presenter</span></span>](ink-presenter.md)<br/> | <span data-ttu-id="4b914-109">Las API del presentador de tinta permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de entradas manuscritas (estándar y modificado) a través de un objeto [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) insertado en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b914-109">The ink presenter APIs enable Microsoft Win32 apps to manage the input, processing, and rendering of ink input (standard and modified) through an [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) object inserted into the app's [DirectComposition](../directcomp/directcomposition-portal.md) visual tree.</span></span><br/> |
| [<span data-ttu-id="4b914-110">Representador de tinta</span><span class="sxs-lookup"><span data-stu-id="4b914-110">Ink renderer</span></span>](ink-renderer.md)<br/>   | <span data-ttu-id="4b914-111">Las API de [representador de tinta](ink-renderer.md) permiten la representación de trazos de tinta en el contexto de dispositivo de Direct2D designado de una aplicación universal de Windows, en lugar del control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4b914-111">The [Ink renderer](ink-renderer.md) APIs enable the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span><br/>                                                                        |

## <a name="related-topics"></a><span data-ttu-id="4b914-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b914-112">Related topics</span></span>

<span data-ttu-id="4b914-113">[Interacciones de lápiz y lápiz](/windows/uwp/design/input/pen-and-stylus-interactions), [ejemplo de análisis de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de entrada de lápiz [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="4b914-113">[Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
