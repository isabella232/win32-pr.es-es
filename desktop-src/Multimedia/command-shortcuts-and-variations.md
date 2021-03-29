---
title: Métodos abreviados de comandos y variaciones
description: Métodos abreviados de comandos y variaciones
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778066"
---
# <a name="command-shortcuts-and-variations"></a>Métodos abreviados de comandos y variaciones

Puede usar varios métodos abreviados al trabajar con comandos MCI. Estos métodos abreviados le permiten usar un único identificador para hacer referencia a todos los dispositivos que ha abierto la aplicación, o para abrir un dispositivo sin emitir explícitamente un comando [**abrir**](open.md) ([**MCI \_ abierto**](mci-open.md)).

Puede especificar "All" (MCI \_ All \_ Device \_ ID) como un identificador de dispositivo para cualquier comando que no devuelva información. Cuando se especifica "All", MCI envía el comando secuencialmente a todos los dispositivos abiertos por la aplicación actual.

Por ejemplo, el comando [**cerrar**](close.md) "todo" cierra todos los dispositivos abiertos y el comando [**reproducir**](play.md) "todo" comienza a reproducir todos los dispositivos abiertos por la aplicación. Dado que MCI envía secuencialmente los comandos a los dispositivos MCI, hay un intervalo entre el momento en que el primer y el último dispositivo reciben el comando.

El uso de "todo" es una manera cómoda de difundir un comando a todos los dispositivos, pero no debe confiar en él para sincronizar los dispositivos. el tiempo entre los mensajes puede variar.

Cuando se emite un comando y se especifica un dispositivo que no está abierto, MCI intenta abrir el dispositivo antes de implementar el comando. Las siguientes reglas se aplican a la apertura automática de dispositivos:

-   La característica de apertura automática solo funciona con la interfaz de la cadena de comandos.
-   Se produce un error en la característica de apertura automática para los comandos que son específicos de los controladores de dispositivos personalizados.
-   Los dispositivos abiertos automáticamente no responden a los comandos que usan "All" como nombre de dispositivo.
-   La característica de apertura automática no permite que la aplicación especifique la marca "tipo". Sin el nombre del dispositivo, MCI determina el nombre del dispositivo a partir de las entradas del registro. Para usar un dispositivo específico, puede combinar el nombre del dispositivo con el nombre de archivo mediante el signo de exclamación, como se describe en el material de referencia del comando [**Open**](open.md) .

Si una aplicación usa la característica de apertura automática para abrir un dispositivo, la aplicación debe comprobar el valor devuelto de cada comando abierto subsiguiente para comprobar que el dispositivo sigue abierto. MCI también cierra automáticamente cualquier dispositivo que se abre automáticamente. MCI normalmente cierra un dispositivo en las siguientes situaciones:

-   El comando se ha completado.
-   Anula el comando.
-   La notificación se solicita en un comando posterior.
-   MCI detecta un error.

 

 




