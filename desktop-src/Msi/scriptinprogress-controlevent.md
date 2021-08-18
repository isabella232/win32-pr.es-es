---
description: El instalador usa este evento para mostrar una cadena de información mientras se compila el script de ejecución de la instalación.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b2e92baf6f1ad3fd4a7ffb714aede88dc90d664564dd5d18f4c97e4d3bdc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041425"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent

El instalador usa este evento para mostrar una cadena de información mientras se compila el script de ejecución de la instalación. La cadena de información se puede mostrar en un cuadro de diálogo mediante un [control text](text-control.md) que se suscribe a este control ControlEvent. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este control ControlEvent se puede controlar mediante una [](r-gly.md)interfaz de usuario que se ejecuta en los niveles de interfaz de usuario [*básica,*](b-gly.md)interfaz de usuario reducida o interfaz [*de usuario*](f-gly.md) completa. Para obtener información sobre los niveles de interfaz de usuario, [vea Interfaz de usuario niveles](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

El instalador publica este control ControlEvent.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en suscriptores

Un [control Text](text-control.md) que se suscriba a ScriptInProgress mostrará la cadena de texto especificada en la tabla [UIText](uitext-table.md).

## <a name="typical-use"></a>Uso típico

Mientras se compila el script de ejecución, el instalador muestra una barra de progreso que indica el tiempo restante antes del principio de la ejecución del script. El autor del paquete puede mostrar un mensaje preliminar en este momento en el que se explica la barra de progreso. Para mostrar un mensaje preliminar, incluya un [control Texto en](text-control.md) el mismo cuadro de diálogo no modelo que progressBar. Especifique que este control Text se suscriba al control ScriptInProgress a través de [la tabla EventMapping](eventmapping-table.md). Incluya una entrada en la [tabla UIText](uitext-table.md) con ScriptInProgress especificado en el campo Clave. Especifique el mensaje preliminar como una cadena de texto en el campo Texto de la tabla UIText. Después, durante la compilación del script, el instalador mostrará esta cadena en el control de texto. El texto mostrado desaparece en cuanto finaliza la compilación del script.

El mismo control de texto que se suscribe a ScriptInProgress ControlEvent también puede suscribirse a [TimeRemaining ControlEvent](timeremaining-controlevent.md). En este caso, a medida que desaparece el texto de la cadena ScriptInProgress preliminar, se reemplaza por la cadena "Tiempo restante: xx minutos".

 

 



