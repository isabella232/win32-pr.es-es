---
description: El evento SetInstallLevel cambia el nivel de instalación al valor especificado por el argumento .
ms.assetid: 71cfd516-4a92-446c-bd8f-a3a04dba0bb2
title: SetInstallLevel ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3e7632e666dc169318e04cbcaf979aa82432d028cc6b7230e6a5e711350ef35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625113"
---
# <a name="setinstalllevel-controlevent"></a>SetInstallLevel ControlEvent

El evento SetInstallLevel cambia el nivel de instalación al valor especificado por el argumento .

Este evento se puede publicar mediante un [control PushButton o](pushbutton-control.md)un [control SelectionTree](selectiontree-control.md). Este evento debe crearse en la [tabla ControlEvent](controlevent-table.md).

Este control ControlEvent requiere que la interfaz de usuario se ejecute en el [*nivel completo de la interfaz de*](f-gly.md) usuario. Este evento no funcionará con una interfaz de usuario [*reducida o*](r-gly.md) una interfaz de [*usuario básica.*](b-gly.md) Para obtener información, [vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Entero que es el nuevo valor del nivel de instalación.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un [control PushButton](pushbutton-control.md) de un cuadro de diálogo modal está asociado a este evento en la [tabla ControlEvent](controlevent-table.md) para cambiar el nivel de instalación.

 

 



