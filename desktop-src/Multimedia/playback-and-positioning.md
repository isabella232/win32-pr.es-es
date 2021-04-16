---
title: Reproducir y colocar
description: Reproducir y colocar
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651296"
---
# <a name="playback-and-positioning"></a>Reproducir y colocar

Una serie de comandos de MCI, como [**reproducir**](play.md) ([**MCI \_ Play**](mci-play.md)), [**detener**](stop.md) ([**MCI \_ Stop**](mci-stop.md)), [**pausar**](pause.md) (MCI [**\_ PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**\_ reanudación de MCI**](mci-resume.md)) y [**búsqueda**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), afectan a la reproducción o la ubicación de un archivo multimedia. Si un dispositivo MCI recibe un comando de reproducción mientras otro comando de reproducción está en curso, acepta el comando y detiene o reemplaza el comando anterior.

Muchos comandos de MCI, como [**set**](set.md) ([**\_ conjunto de MCI**](mci-set.md)), no afectan a la reproducción. Una notificación de uno de estos comandos no interfiere con los comandos de reproducción o posición pendientes, siempre y cuando las notificaciones no se realicen desde la misma instancia del controlador. Por ejemplo, puede emitir un comando **set** o [**status**](status.md) ([**\_ Estado de MCI**](mci-status.md)) mientras un dispositivo está realizando un comando **Seek** sin detener o reemplazar el comando **Seek** .

Sin embargo, solo puede haber una notificación pendiente. Por ejemplo, si una aplicación solicita una notificación para que se **reproduzca** y sigue a esa solicitud con el **Estado** "Start Position Notify", la notificación de **reproducción** devolverá "Returned" y la notificación del comando status devolverá cuando termine. Sin embargo, en este caso, el comando **Play** seguirá teniendo éxito, aunque la aplicación no haya recibido la notificación.

 

 




