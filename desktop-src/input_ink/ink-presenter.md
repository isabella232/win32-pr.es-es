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
# <a name="ink-presenter"></a>Presentador de tinta

Las API del presentador de tinta permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de entradas manuscritas (estándar y modificado) a través de un objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) insertado en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.

> [!Note]
>
> La entrada de lápiz estándar (sugerencia o botón de la punta del lápiz o del borrador) no se modifica con una prestación secundaria, como un botón de barril del lápiz, un botón secundario del mouse o similar.

Las aplicaciones Plataforma universal de Windows (UWP) que usan lenguaje XAML (XAML) proporcionan esta funcionalidad a través de un control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) junto con un objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) que se conecta al árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de XAML. Para obtener más información, consulte [interacciones de lápiz y](/windows/uwp/design/input/pen-and-stylus-interactions)lápiz.

El [representador de tinta](ink-renderer.md) está diseñado para que lo usen los desarrolladores de aplicaciones universales de Windows interesados en proporcionar la funcionalidad de InkPresenter de [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)basada en XAML / [](/uwp/api/windows.ui.input.inking.inkpresenter) en aplicaciones Win32 nativas.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Clases de presentador de tinta](ink-presenter-classes.md)<br/>       | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para las clases de presentador de tinta. <br/>    |
| [Interfaces de presentador de tinta](ink-presenter-interfaces.md)<br/> | Los temas contenidos en esta sección proporcionan las especificaciones de referencia de las interfaces de presentación de tinta. <br/> |



 

## <a name="related-topics"></a>Temas relacionados

[Presentador de tinta](ink-presenter.md), [interacciones de lápiz y lápiz óptico](/windows/uwp/design/input/pen-and-stylus-interactions), ejemplo de análisis de [tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de entrada de lápiz [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)
