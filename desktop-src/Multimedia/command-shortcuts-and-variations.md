---
title: Métodos abreviados de comandos y variaciones
description: Métodos abreviados de comandos y variaciones
ms.assetid: 4f854c78-435c-4a10-8938-645ad605fff3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82ce41aaa9cc5744a2f199a7f7761111734e848
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069566"
---
# <a name="command-shortcuts-and-variations"></a>Métodos abreviados de comandos y variaciones

Puede usar varios accesos directos al trabajar con comandos MCI. Estos accesos directos permiten usar un único identificador para hacer referencia a todos los dispositivos que la aplicación ha abierto o para abrir un dispositivo sin emitir explícitamente un comando [**open**](open.md) [**(MCI \_ OPEN).**](mci-open.md)

Puede especificar "all" (MCI ALL DEVICE ID) como identificador de dispositivo para \_ cualquier comando que no devuelva \_ \_ información. Cuando se especifica "all", MCI envía el comando secuencialmente a todos los dispositivos abiertos por la aplicación actual.

Por ejemplo, el [**comando cerrar**](close.md) "todos" cierra todos los dispositivos abiertos y el comando [**"todos"**](play.md) de reproducción empieza a reproducir todos los dispositivos abiertos por la aplicación. Dado que MCI envía secuencialmente los comandos a los dispositivos MCI, hay un intervalo entre el momento en que el primer y el último dispositivo reciben el comando.

El uso de "all" es una manera cómoda de difundir un comando a todos los dispositivos, pero no debe confiar en él para sincronizar los dispositivos. el tiempo entre mensajes puede variar.

Cuando se emite un comando y se especifica un dispositivo que no está abierto, MCI intenta abrir el dispositivo antes de implementar el comando. Las siguientes reglas se aplican a la apertura automática de dispositivos:

-   La característica de apertura automática solo funciona con la interfaz de cadena de comandos.
-   Se produce un error en la característica de apertura automática para los comandos específicos de los controladores de dispositivos personalizados.
-   Los dispositivos abiertos automáticamente no responden a los comandos que usan "all" como nombre de dispositivo.
-   La característica de apertura automática no permite que la aplicación especifique la marca "type". Sin el nombre del dispositivo, MCI determina el nombre del dispositivo a partir de las entradas del registro. Para usar un dispositivo específico, puede combinar el nombre del dispositivo con el nombre de archivo mediante el signo de exclamación, como se describe en el material de referencia para el [**comando open.**](open.md)

Si una aplicación usa la característica de apertura automática para abrir un dispositivo, la aplicación debe comprobar el valor devuelto de cada comando abierto posterior para comprobar que el dispositivo sigue abierto. MCI también cierra automáticamente cualquier dispositivo que se abra automáticamente. MCI normalmente cierra un dispositivo en las situaciones siguientes:

-   El comando se ha completado.
-   Anule el comando.
-   Se solicita una notificación en un comando posterior.
-   MCI detecta un error.

 

 




