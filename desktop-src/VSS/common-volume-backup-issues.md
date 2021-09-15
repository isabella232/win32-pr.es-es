---
description: 'Cualquier operación de copia de seguridad que intente copiar una imagen completa y estable de un sistema debe abordar los siguientes problemas:'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problemas comunes de copia de seguridad de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f10433e0a695c11f7e61a258c3256baa651dc27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473392"
---
# <a name="common-volume-backup-issues"></a>Problemas comunes de copia de seguridad de volumen

Cualquier operación de copia de seguridad que intente copiar una imagen completa y estable de un sistema debe abordar los siguientes problemas:

-   Archivos inaccesibles durante una copia de seguridad. La ejecución de aplicaciones con frecuencia necesita mantener los archivos abiertos en modo exclusivo durante una copia de seguridad, lo que impide que los programas de copia de seguridad los copien.
-   Estado de archivo incoherente. Incluso si una aplicación no tiene sus archivos abiertos en modo exclusivo, es posible, debido al tiempo finito necesario para abrir, realizar copias de seguridad y cerrar un archivo, es posible que los archivos copiados en los medios de almacenamiento no reflejen el mismo estado de la aplicación.
-   Es necesario minimizar las interrupciones del servicio. Para garantizar la accesibilidad de los archivos y la integridad de los datos de los que se va a realizar una copia de seguridad, es necesario suspender o finalizar todos los programas en ejecución durante una copia de seguridad de volumen. En el caso de los sistemas de disco de gran tamaño, esta duración podría ser de horas.

    Recientemente, algunos proveedores de almacenamiento han intentado solucionar estos problemas proporcionando un mecanismo de captura de volumen (un medio para capturar una imagen de los archivos en disco en un momento dado en el tiempo) mediante un mecanismo de copia en escritura o "reflejo dividido". Sin embargo, estas soluciones implican dificultades propias:

    -   Implementaciones de proveedor incompatibles de captura de volumen. Muchos proveedores de dispositivos RAID proporcionan mecanismos de captura de volumen. Sin embargo, cada proveedor tiene su propia interfaz y cada uno debe obtener soporte técnico de los proveedores de copia de seguridad para sus interfaces de captura de volumen. Esto significa que los proveedores de aplicaciones de copia de seguridad deben admitir varias implementaciones de captura de volumen, lo que no es deseable.
    -   Falta de coordinación de aplicaciones. Muchos dispositivos que admiten una captura de volumen no admiten la coordinación de la ejecución de aplicaciones con la inmovilización de datos en el disco. Para los dispositivos que sí lo hacen, al igual que con las aplicaciones de copia de seguridad, cada proveedor tiene una interfaz diferente.
    -   Compatibilidad limitada con dispositivos que no son RAID. Pocos proveedores de discos convencionales proporcionan compatibilidad con cualquier tipo de captura de volumen en sus controladores de dispositivo. Esto significa que los mecanismos de captura se limitan a determinados sistemas de disco y normalmente no admiten la copia de seguridad de áreas del sistema.
    -   Debe controlar las actualizaciones del disco durante la captura de volumen. Aunque los mecanismos de captura de volúmenes proporcionados por el proveedor de almacenamiento pueden inmovilizar el estado de los datos en el disco, no siempre interoperan con las aplicaciones en ejecución. Esto suele significar que se pueden perder los datos enviados al volumen mientras un dispositivo de almacenamiento se somete a la captura de volumen.
    -   Copia de seguridad coherente de variasvolume. El dispositivo de almacenamiento ejecuta estas capturas de volumen, por lo que por lo general no hay ningún mecanismo para coordinar el tiempo de inmovilización de los datos. Esto es especialmente cierto si los dispositivos proceden de proveedores independientes. Por lo tanto, si hay varios volúmenes de almacenamiento implicados en una copia de seguridad con una captura de volumen, es posible que la imagen de tiempo conservada para cada volumen no sea coherente.

 

 



