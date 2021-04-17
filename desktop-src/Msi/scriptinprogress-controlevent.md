---
description: El instalador usa este evento para mostrar una cadena informativa mientras se está compilando el script de ejecución de la instalación.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652687"
---
# <a name="scriptinprogress-controlevent"></a>ScriptInProgress ControlEvent,

El instalador usa este evento para mostrar una cadena informativa mientras se está compilando el script de ejecución de la instalación. La cadena informativa se puede mostrar en un cuadro de diálogo mediante un [control de texto](text-control.md) que se suscribe a este ControlEvent,. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) . Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Un [control de texto](text-control.md) que se suscribe a ScriptInProgress mostrará la cadena de texto especificada en la [tabla UIText](uitext-table.md).

## <a name="typical-use"></a>Uso típico

Mientras se está compilando el script de ejecución, el instalador muestra un componente ProgressBar que indica el tiempo restante antes del inicio de la ejecución del script. En este momento, el autor del paquete puede mostrar un mensaje preliminar que explica el ProgressBar. Para mostrar un mensaje preliminar, incluya un [control de texto](text-control.md) en el mismo cuadro de diálogo no modal que ProgressBar. Especifica que este control de texto se suscribe a ScriptInProgress ControlEvent, a través de la [tabla EventMapping](eventmapping-table.md). Incluya una entrada en la [tabla UIText](uitext-table.md) con ScriptInProgress especificado en el campo clave. Especifique el mensaje preliminar como una cadena de texto en el campo de texto de la tabla UIText. Después, durante la compilación del script, el instalador mostrará esta cadena en el control de texto. El texto mostrado desaparece en cuanto finaliza la compilación del script.

El mismo control de texto que se suscribe a ScriptInProgress ControlEvent, también puede suscribirse a [TimeRemaining ControlEvent,](timeremaining-controlevent.md). En este caso, como el texto de la cadena de ScriptInProgress preliminar desaparece, se reemplaza por la cadena "tiempo restante: XX minutos".

 

 



