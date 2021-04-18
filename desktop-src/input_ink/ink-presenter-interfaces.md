---
description: Los temas contenidos en esta sección proporcionan las especificaciones de referencia de las interfaces de presentación de tinta.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfaces de presentador de tinta
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 1839c8ebc0a7597ab7c5becaf7c7492128b4d6af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720505"
---
# <a name="ink-presenter-interfaces"></a>Interfaces de presentador de tinta

Los temas contenidos en esta sección proporcionan las especificaciones de referencia de las interfaces de [presentación de tinta](ink-presenter.md) .

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Habilita la aplicación (en lugar de un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) ) para confirmar todos los comandos de DirectComposition de Microsoft pendientes en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Habilita la entrada de lápiz, el procesamiento y la representación a través de la creación de un subproceso de aplicación para hospedar un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e insertarlo en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Representa una operación de entrada de lápiz que se va a ejecutar en un subproceso de objeto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) .<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Representa un [**objeto InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) que se puede configurar e insertar en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación clásica de Windows. <br/>                                        |

## <a name="related-topics"></a>Temas relacionados

[Presentador de tinta](ink-presenter.md), [interacciones de lápiz y lápiz óptico](/windows/uwp/design/input/pen-and-stylus-interactions), ejemplo de análisis de [tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de entrada de lápiz [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)
