---
description: El instalador usa el evento SetProgress para publicar información sobre el progreso de la instalación.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272404"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent

El instalador usa el evento SetProgress para publicar información sobre el progreso de la instalación. Un [control ProgressBar o](progressbar-control.md) Control [Desenlace](billboard-control.md) debe suscribirse al evento a través de la tabla [EventMapping;](eventmapping-table.md) para ello, debe asignar un nombre a la acción cuyo progreso se indica. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent se puede controlar mediante una [](r-gly.md)interfaz de usuario que se ejecuta en los niveles básico de interfaz de [*usuario,*](b-gly.md)interfaz de usuario reducida o interfaz [*de usuario*](f-gly.md) completa. Para obtener información sobre los niveles de interfaz de [usuario, vea Interfaz de usuario Levels](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [ProgressBar](progressbar-control.md) en un cuadro de diálogo modeless se suscribe a este evento mediante el [atributo Progress](progress-control-attribute.md) para recibir la información de progreso.

 

 



