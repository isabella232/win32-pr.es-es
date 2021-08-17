---
description: Las API de moderador de lápiz permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de entrada de lápiz (estándar o modificada) a través de un objeto InkPresenter insertado en el árbol visual DirectComposition de la aplicación.
ms.assetid: 8BD52813-3741-4C1F-B62A-B3C366A86362
title: Presentador de ink
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: ccd201f39cf232e91c65d8ef15c6ccc0e8202b231818aa50d34d70f780f2d9e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977025"
---
# <a name="ink-presenter"></a>Presentador de ink

Las API de presentador de entrada de lápiz permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de la entrada de lápiz (estándar y modificada) a través de un objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) insertado en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.

> [!Note]
>
> La entrada de lápiz estándar (punta de lápiz o punta de borrador o botón) no se modifica con una asequibilidad secundaria, como un botón de lápiz, un botón derecho del mouse o similar.

Las aplicaciones Windows Plataforma universal de Windows (UWP) que usan lenguaje XAML (XAML) proporcionan esta funcionalidad a través de un control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) junto con un objeto [**InkPresenter**](/uwp/api/windows.ui.input.inking.inkpresenter) que se conecta al árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de XAML. Para obtener más detalles, vea [Interacciones de lápiz y lápiz.](/windows/uwp/design/input/pen-and-stylus-interactions)

[El representador de ink](ink-renderer.md) está diseñado para su uso por desarrolladores de aplicaciones Windows universales interesados en proporcionar la funcionalidad [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)InkPresenter basada en XAML en aplicaciones / [](/uwp/api/windows.ui.input.inking.inkpresenter) Win32 nativas.

## <a name="in-this-section"></a>En esta sección



| Tema                                                               | Descripción                                                                                                         |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Clases de presentador de ink](ink-presenter-classes.md)<br/>       | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para las clases de presentador de Ink. <br/>    |
| [Interfaces de presentador de ink](ink-presenter-interfaces.md)<br/> | Los temas contenidos en esta sección proporcionan las especificaciones de referencia para las interfaces de presentador de Ink. <br/> |



 

## <a name="related-topics"></a>Temas relacionados

[Presentador de lápiz,](ink-presenter.md) [interacciones de lápiz y lápiz,](/windows/uwp/design/input/pen-and-stylus-interactions)ejemplo de análisis de lápiz, ejemplo de entrada manuscrita [simple,](/samples/microsoft/windows-universal-samples/simpleink/) [ejemplo de entrada manuscrita compleja](/samples/microsoft/windows-universal-samples/complexink/) [](/samples/microsoft/windows-universal-samples/inkanalysis/)
