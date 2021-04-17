---
description: 'Cualquier operación de copia de seguridad que intente copiar una imagen completa y estable de un sistema debe tratar los siguientes aspectos:'
ms.assetid: 8ccdba6d-1097-4c1c-982c-f3d9cbdf06cd
title: Problemas comunes de copia de seguridad de volumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f10433e0a695c11f7e61a258c3256baa651dc27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653045"
---
# <a name="common-volume-backup-issues"></a>Problemas comunes de copia de seguridad de volumen

Cualquier operación de copia de seguridad que intente copiar una imagen completa y estable de un sistema debe tratar los siguientes aspectos:

-   Archivos inaccesibles durante una copia de seguridad. Con frecuencia, las aplicaciones en ejecución necesitan mantener los archivos abiertos en modo exclusivo durante una copia de seguridad, evitando que los programas de copia de seguridad los copien.
-   Estado de archivo incoherente. Incluso si una aplicación no tiene sus archivos abiertos en modo exclusivo, es posible que, debido al tiempo finito necesario para abrir, realizar una copia de seguridad y cerrar un archivo, los archivos copiados en el medio de almacenamiento no reflejen el mismo estado de la aplicación.
-   Necesidad de minimizar las interrupciones del servicio. Para garantizar la accesibilidad de los archivos y la integridad de los datos de los que se realiza una copia de seguridad, es posible que se requiera la suspensión o finalización de todos los programas en ejecución durante una copia de seguridad del volumen. En el caso de los sistemas de discos de gran tamaño, esto podría ser horas de duración.

    Recientemente, algunos proveedores de almacenamiento han intentado resolver estos problemas proporcionando un mecanismo de captura de volumen, un medio para capturar una imagen de los archivos en disco en un momento dado en el tiempo, mediante un mecanismo de copia en escritura o de "reflejo dividido". Sin embargo, estas soluciones suponen dificultades propias:

    -   Implementaciones de los proveedores incompatibles de la captura de volumen. Muchos proveedores de dispositivos RAID proporcionan mecanismos de captura de volumen. Sin embargo, cada proveedor tiene su propia interfaz y cada uno debe obtener soporte técnico de los proveedores de copia de seguridad para sus interfaces de captura de volumen. Esto significa que los proveedores de aplicaciones de copia de seguridad deben admitir varias implementaciones de captura de volumen, lo cual no es deseable.
    -   Falta de coordinación de la aplicación. Muchos dispositivos que admiten una captura de volumen no admiten la coordinación de la ejecución de aplicaciones con la inmovilización de datos en el disco. En el caso de los dispositivos que hacen, al igual que las aplicaciones de copia de seguridad, cada proveedor tiene una interfaz diferente.
    -   Compatibilidad limitada para dispositivos que no son RAID. Pocos si los proveedores de discos convencionales proporcionan compatibilidad con cualquier tipo de captura de volumen en sus controladores de dispositivos. Esto significa que los mecanismos de captura se limitan a determinados sistemas de disco y, por lo general, no admiten la copia de seguridad de áreas del sistema.
    -   Es necesario controlar las actualizaciones del disco durante la captura de volumen. Aunque los mecanismos de captura de volumen proporcionados por el proveedor de almacenamiento pueden inmovilizar el estado de los datos en el disco, no siempre interoperan con las aplicaciones en ejecución. Esto suele significar que se pueden perder los datos que se envían al volumen mientras un dispositivo de almacenamiento está llevando a cabo una captura de volumen.
    -   Copia de seguridad de multivolumen coherente. El dispositivo de almacenamiento ejecuta estas capturas de volumen, por lo que normalmente no hay ningún mecanismo para coordinar la temporización de la inmovilización de datos. Esto es especialmente cierto si los dispositivos proceden de proveedores independientes. Por lo tanto, si hay varios volúmenes de almacenamiento implicados en una copia de seguridad con una captura de volumen, es posible que la imagen de tiempo conservada para cada volumen no sea coherente.

 

 



