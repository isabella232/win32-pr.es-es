---
description: Los temas contenidos en esta sección proporcionan las especificaciones de referencia para las interfaces de presentador de Ink.
ms.assetid: 68172566-586C-41AC-82B8-5DBE8B50EC8F
title: Interfaces de presentador de entrada manuscrita
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 0c1fb4cab0b8387dec7c75087a72719f72fbc85dc2776a5e20fc6d638fb02d95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092395"
---
# <a name="ink-presenter-interfaces"></a>Interfaces de presentador de entrada manuscrita

Los temas contenidos en esta sección proporcionan las especificaciones de referencia para las interfaces [de presentador de](ink-presenter.md) Ink.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**IInkCommitRequestHandler**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkcommitrequesthandler)<br/> | Permite que la aplicación (en lugar de un objeto [**IInkPresenterDesktop)**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) confirme todos los comandos pendientes de Microsoft DirectComposition en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.<br/>   |
| [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)<br/>                   | Permite la entrada de lápiz, el procesamiento y la representación mediante la creación de un subproceso de aplicación para hospedar un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e insertarlo en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación. <br/> |
| [**IInkHostWorkItem**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkhostworkitem)<br/>                 | Representa una operación de entrada de lápiz que se va a ejecutar en un [**subproceso de objeto IInkDesktopHost.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>                                                                                                                                                  |
| [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)<br/>         | Representa un [**objeto InkPresenter**](/uwp/api/Windows.UI.Input.Inking.InkPresenter) que se puede configurar e insertar en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación Windows clásica. <br/>                                        |

## <a name="related-topics"></a>Temas relacionados

[Presentador de entrada de](ink-presenter.md)lápiz, [interacciones de lápiz y](/windows/uwp/design/input/pen-and-stylus-interactions) [lápiz,](/samples/microsoft/windows-universal-samples/inkanalysis/)ejemplo de análisis de entrada de lápiz, ejemplo de entrada manuscrita [simple,](/samples/microsoft/windows-universal-samples/simpleink/) [ejemplo de entrada manuscrita compleja](/samples/microsoft/windows-universal-samples/complexink/)
