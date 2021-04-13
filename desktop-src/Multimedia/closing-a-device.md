---
title: Cerrar un dispositivo
description: Cerrar un dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Comando MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418402"
---
# <a name="closing-a-device"></a>Cerrar un dispositivo

El comando [**cerrar**](close.md) ([**\_ cerrar MCI**](mci-close.md)) libera el acceso a un dispositivo o a un archivo. MCI libera un dispositivo cuando todas las tareas que usan un dispositivo lo han cerrado. Para ayudar a MCI a administrar los dispositivos, la aplicación debe cerrar cada dispositivo o archivo cuando haya terminado de usarlo.

Cuando se cierra un dispositivo MCI externo que usa su propio medio en lugar de archivos (por ejemplo, audio de CD), el controlador deja el dispositivo en su modo de funcionamiento actual. Por lo tanto, si cierra un dispositivo de audio de CD que se está reproduciendo, aunque el controlador de dispositivo se libere de la memoria, el dispositivo de audio de CD seguirá reproduciéndose hasta que llegue al final de su contenido.

> [!Note]  
> Cerrar una aplicación con dispositivos MCI abiertos puede impedir que otras aplicaciones usen esos dispositivos hasta que se reinicie Windows.

 

 

 




