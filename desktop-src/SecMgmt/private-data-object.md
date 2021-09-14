---
description: Hay un número limitado de objetos de datos privados disponibles en cada sistema con el fin de almacenar información de forma protegida, cifrada.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Objeto de datos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071134"
---
# <a name="private-data-object"></a>Objeto de datos privados

Hay un número limitado de objetos de datos privados disponibles en cada sistema con el fin de almacenar información de forma protegida, cifrada.

Los objetos de datos privados se proporcionan principalmente para admitir el almacenamiento de contraseñas de cuenta de servidor. Esto es útil para los servidores que se ejecutan en una cuenta específica. La contraseña de la cuenta de servidor son datos privados que deben protegerse, pero que son necesarios para iniciar sesión en el servidor.

Los objetos de datos privados pueden ser de uso general o pueden ser uno de los tres tipos especializados: local, global y máquina.

Los objetos de datos privados locales solo se pueden leer localmente desde el equipo que almacena el objeto. Al intentar leerlos de forma remota, se produce un error ACCESO \_ \_ DENEGADO DE ESTADO. Los objetos de datos privados locales tienen nombres de clave que comienzan con el prefijo "L$". Además de los objetos privados locales que se crean, el sistema operativo define los siguientes objetos privados locales: $machine.acc, SAC, SAI y SANSC.

Los objetos de datos privados globales son globales en el sentido de que si se crean en un controlador de dominio, se replicarán automáticamente en todos los controladores de dominio de ese dominio. En otras palabras, cada controlador de dominio de ese dominio tendrá acceso a los valores que contiene el objeto de datos privado global. En cambio, los objetos de datos privados globales creados en un sistema que no es un controlador de dominio, así como los objetos de datos privados no globales, no se replican. Los objetos de datos privados globales tienen nombres de clave que comienzan por "G$".

Solo el sistema operativo puede acceder a los objetos de datos privados de la máquina. Estos objetos tienen nombres de clave que comienzan por "M$".

**Nota**  Puede establecer, pero no recuperar, objetos de datos privados de la máquina.

Además de estos prefijos, los valores siguientes también indican objetos locales o de máquina. Estos valores se admiten por compatibilidad con versiones anteriores y no se deben usar al crear nuevos objetos locales o de máquina. El nombre de clave de los objetos de datos privados locales también puede empezar por "RasDialParms" o "RasCredentials". El nombre de clave de los objetos de máquina también puede empezar por "NL$" o " \_ sc \_ ".

Los objetos de datos privados que no son uno de los tipos especializados anteriores usan nombres de clave que no comienzan con un prefijo. Estos objetos no se replican y las aplicaciones pueden leer de forma local o remota.

 

 



