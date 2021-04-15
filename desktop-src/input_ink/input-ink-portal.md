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
# <a name="ink-input"></a>Entrada manuscrita

Obtenga información sobre las distintas API de entrada manuscrita de escritorio para aplicaciones Windows.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [Presentador de tinta](ink-presenter.md)<br/> | Las API del presentador de tinta permiten a las aplicaciones de Microsoft Win32 administrar la entrada, el procesamiento y la representación de entradas manuscritas (estándar y modificado) a través de un objeto [**InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) insertado en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.<br/> |
| [Representador de tinta](ink-renderer.md)<br/>   | Las API de [representador de tinta](ink-renderer.md) permiten la representación de trazos de tinta en el contexto de dispositivo de Direct2D designado de una aplicación universal de Windows, en lugar del control [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) predeterminado.<br/>                                                                        |

## <a name="related-topics"></a>Temas relacionados

[Interacciones de lápiz y lápiz](/windows/uwp/design/input/pen-and-stylus-interactions), [ejemplo de análisis de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de entrada de lápiz [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)
