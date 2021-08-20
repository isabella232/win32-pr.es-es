---
title: Cerrar un dispositivo
description: Cerrar un dispositivo
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- MCI_CLOSE comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f81ddaf42ef5509b55271159b8e36ac56584b92734a6b04e5b555041596530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498085"
---
# <a name="closing-a-device"></a>Cerrar un dispositivo

El [**comando close**](close.md) [**(MCI \_ CLOSE)**](mci-close.md)libera el acceso a un dispositivo o archivo. MCI libera un dispositivo cuando todas las tareas que usan un dispositivo lo han cerrado. Para ayudar a MCI a administrar los dispositivos, la aplicación debe cerrar cada dispositivo o archivo cuando haya terminado de usarlo.

Cuando se cierra un dispositivo MCI externo que usa su propio medio en lugar de archivos (como audio de CD), el controlador deja el dispositivo en su modo de funcionamiento actual. Por lo tanto, si cierra un dispositivo de audio de CD que se está reproduciendo, aunque el controlador del dispositivo se libera de la memoria, el dispositivo de audio de CD seguirá reproduciendo hasta que llegue al final de su contenido.

> [!Note]  
> El cierre de una aplicación con dispositivos MCI abiertos puede impedir que otras aplicaciones utilicen esos dispositivos hasta Windows se reinicie.

 

 

 




