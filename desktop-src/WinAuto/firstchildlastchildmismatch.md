---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418887"
---
# <a name="firstchildlastchildmismatch"></a>FirstChildLastChildMismatch

## <a name="text"></a>Texto

Al navegar llamando {0} desde el nodo probado y, a continuación, llamando repetidamente a {1} , finalizamos en el siguiente elemento secundario: {2} . Esto no coincidía con el resultado de llamar a {3} en el nodo probado, que produjo: {4} . En su lugar, el elemento secundario debe notificar como elemento primario el nodo de prueba.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Hay un problema al desplazarse entre los elementos secundarios de un elemento. 1. Implementación de automatización de la interfaz de usuario incorrecta o no válida.

Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.

## <a name="possible-causes"></a>Causas posibles

Implementación de automatización de la interfaz de usuario incorrecta o no válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IUIAutomationElement::GetCachedParent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




