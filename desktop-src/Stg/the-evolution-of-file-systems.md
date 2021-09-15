---
title: La evolución de los sistemas de archivos
description: Antes de que los equipos se desarrollaron para funcionar en sistemas operativos de disco, cada equipo se creó para ejecutar una única aplicación propietaria, que tenía un control completo y exclusivo de toda la máquina.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc34dc699488b5952d52dfd13f49ea63aaa85aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270559"
---
# <a name="the-evolution-of-file-systems"></a>La evolución de los sistemas de archivos

Antes de que los equipos se desarrollaron para funcionar en sistemas operativos de disco, cada equipo se creó para ejecutar una única aplicación propietaria, que tenía un control completo y exclusivo de toda la máquina. La aplicación escribiría sus datos persistentes directamente en un disco, o bien, mediante el envío de comandos directamente al controlador de disco. La aplicación era responsable de administrar las ubicaciones absolutas de los datos en el disco, asegurando de que no sobrescribía los datos ya existentes. Puesto que solo se estaba ejecutando una aplicación en el equipo en cualquier momento, esta tarea no era demasiado difícil.

La llegada de los sistemas informáticos que podían ejecutar más de una aplicación requería un mecanismo para asegurarse de que las aplicaciones no escriben sobre los datos de los demás. Los desarrolladores de aplicaciones abordaron este problema mediante la adopción de un único estándar para distinguir los sectores de disco en uso de los que estaban libres al marcarlos en consecuencia. Con el tiempo, estos estándares se han convertido en un sistema operativo de disco, que proporciona varios servicios a las aplicaciones, incluido un sistema de archivos para administrar el almacenamiento persistente. Con la llegada de un sistema de archivos, las aplicaciones ya no tenían que tratar directamente con el medio de almacenamiento físico. En su lugar, simplemente le han dicho al sistema de archivos que escriba bloques de datos en el disco y deje que el sistema de archivos se preocupe por cómo hacerlo. Además, el sistema de archivos permitía a las aplicaciones crear jerarquías de datos a través de una abstracción conocida como directorio. Un directorio podría contener no solo archivos, sino también otros directorios, que a su vez podrían contener sus propios archivos y directorios, y así sucesivamente.

El sistema de archivos proporcionaba un único nivel de direccionamiento indirecto entre las aplicaciones y el disco, y el resultado era que cada aplicación veba un archivo como una única secuencia contigua de bytes en el disco, aunque el sistema de archivos almacenase realmente el archivo en sectores imprevistos. El direccionamiento indirecto liberaba a las aplicaciones de tener que realizar un seguimiento de la posición absoluta de los datos en un dispositivo de almacenamiento.

En la actualidad, prácticamente todas las API del sistema para la entrada y salida de archivos proporcionan aplicaciones para escribir información en un archivo plano. Las aplicaciones ven este archivo como una sola secuencia de bytes que puede crecer tanto como sea necesario hasta que el disco esté lleno. Durante mucho tiempo, estas API han sido suficientes para que las aplicaciones almacenen su información persistente. Las aplicaciones han realizado innovaciones significativas en la forma en que tratan con un único flujo de información para proporcionar características como ahorros incrementales "rápidos".

Sin embargo, en un mundo de objetos de componente, el almacenamiento de datos en un único archivo plano ya no es eficaz. Al igual que los sistemas de archivos surgieron de la necesidad de que varias aplicaciones compartan el mismo medio de almacenamiento, por lo que ahora, los objetos de componente requieren un sistema que les permita compartir el almacenamiento dentro del marco conceptual de un solo archivo. Aunque es posible almacenar los objetos independientes mediante el almacenamiento de archivos planos convencional, si uno de los objetos aumenta de tamaño o simplemente agrega otro objeto, es necesario cargar todo el archivo en la memoria, insertar el nuevo objeto y, a continuación, guardar todo el archivo. Este proceso puede llevar mucho tiempo.

La solución proporcionada por COM es implementar un segundo nivel de direccionamiento indirecto: un sistema de archivos dentro de un archivo. El almacenamiento de archivos planos requiere que una secuencia contigua grande de bytes en el disco se manipule a través de un único identificador de archivo con un solo puntero de búsqueda. Por el contrario, el almacenamiento estructurado COM define cómo tratar una única entidad del sistema de archivos como una colección estructurada de dos tipos de objetos (almacenamientos y flujos) que actúan como directorios y archivos.

 

 




