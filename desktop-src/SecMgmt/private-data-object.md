---
description: En cada sistema hay disponible un número limitado de objetos de datos privados con el fin de almacenar información de manera protegida y cifrada.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Private Data, objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154076"
---
# <a name="private-data-object"></a>Private Data, objeto

En cada sistema hay disponible un número limitado de objetos de datos privados con el fin de almacenar información de manera protegida y cifrada.

Los objetos de datos privados se proporcionan principalmente para admitir el almacenamiento de contraseñas de cuentas de servidor. Esto es útil para los servidores que se ejecutan en una cuenta específica. La contraseña de la cuenta de servidor son datos privados que se deben proteger, pero que son necesarios para iniciar sesión en el servidor.

Los objetos de datos privados pueden ser de uso general o pueden ser de uno de los tres tipos especializados: local, global y equipo.

Los objetos de datos privados locales solo se pueden leer localmente desde el equipo que almacena el objeto. Al intentar leerlos de forma remota, se produce un \_ error de acceso \_ denegado de estado. Los objetos de datos privados locales tienen nombres de clave que comienzan con el prefijo "L $". Además de los objetos privados locales que cree, el sistema operativo define los siguientes objetos privados locales: $machine. ACC, SAC, SAI y SANSC.

Los objetos de datos privados globales son globales en el sentido de que, si se crean en un controlador de dominio, se replicarán automáticamente en todos los controladores de dominio de ese dominio. En otras palabras, cada controlador de dominio de ese dominio tendrá acceso a los valores que contiene el objeto de datos privado global. En cambio, los objetos de datos privados globales creados en un sistema que no es un controlador de dominio, así como los objetos de datos privados no globales, no se replican. Los objetos de datos privados globales tienen nombres de clave que empiezan por "G $".

Solo el sistema operativo puede tener acceso a los objetos de datos privados de la máquina. Estos objetos tienen nombres de clave que comienzan por "M $".

**Nota:**  Puede establecer, pero no puede recuperar los objetos de datos privados de la máquina.

Además de estos prefijos, los valores siguientes también indican objetos locales o de equipo. Estos valores se admiten por razones de compatibilidad con versiones anteriores y no se deben usar al crear nuevos objetos locales o de equipo. El nombre de clave de los objetos de datos privados locales también puede comenzar con "RasDialParms" o "RasCredentials". El nombre de clave de los objetos de equipo también puede empezar por "NL $" o " \_ SC \_ ".

Los objetos de datos privados que no son uno de los tipos especializados anteriores utilizan nombres de clave que no se inician con un prefijo. Estos objetos no se replican y las aplicaciones pueden leerlos de forma local o remota.

 

 



