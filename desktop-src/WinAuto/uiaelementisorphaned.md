---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714187"
---
# <a name="uiaelementisorphaned"></a>UiaElementIsOrphaned

## <a name="text"></a>Texto

El elemento es un AutomationElement huérfano en el árbol

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La dirección de la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del objeto obtenida para las coordenadas dadas es una referencia a un elemento huérfano en el árbol de elementos.

Este problema es un problema para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se tratarán como invisibles y no se anunciarán al usuario.

## <a name="possible-causes"></a>Causas posibles

-   Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.
-   Implementación de automatización de la interfaz de usuario incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAutomationElement.ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




