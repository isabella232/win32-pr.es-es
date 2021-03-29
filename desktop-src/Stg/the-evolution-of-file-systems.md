---
title: La evolución de los sistemas de archivos
description: Antes de que los equipos se desarrollaron para funcionar en los sistemas operativos de disco, cada equipo se compiló para ejecutar una única aplicación de propiedad, que tenía un control completo y exclusivo de todo el equipo.
ms.assetid: 46d497b5-c325-4395-8512-1ed4b88441de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc34dc699488b5952d52dfd13f49ea63aaa85aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665641"
---
# <a name="the-evolution-of-file-systems"></a>La evolución de los sistemas de archivos

Antes de que los equipos se desarrollaron para funcionar en los sistemas operativos de disco, cada equipo se compiló para ejecutar una única aplicación de propiedad, que tenía un control completo y exclusivo de todo el equipo. La aplicación escribiría sus datos persistentes directamente en un disco, o tambor, enviando comandos directamente al controlador de disco. La aplicación era responsable de administrar las ubicaciones absolutas de los datos en el disco, asegurándose de que no se sobrescribiran los datos ya existentes. Puesto que solo se estaba ejecutando una aplicación en el equipo en cualquier momento, esta tarea no era demasiado difícil.

La llegada de los sistemas informáticos que podían ejecutar más de una aplicación requiere un mecanismo para asegurarse de que las aplicaciones no han escrito los datos de los demás. Para solucionar este problema, los desarrolladores de aplicaciones adoptan un estándar único para distinguir los sectores de disco en uso de los que estaban libres marcándolos. En el tiempo, estos estándares se fusionaron para convertirse en un sistema operativo de disco, que proporcionaba varios servicios a las aplicaciones, incluido un sistema de archivos para administrar el almacenamiento persistente. Con la llegada de un sistema de archivos, las aplicaciones ya no tenían que tratar directamente con el medio de almacenamiento físico. En su lugar, simplemente indicaban al sistema de archivos que escribira bloques de datos en el disco y dejar que el sistema de archivos se preocupe de cómo hacerlo. Además, el sistema de archivos permitía a las aplicaciones crear jerarquías de datos a través de una abstracción conocida como directorio. Un directorio no puede contener solo archivos y otros directorios que, a su vez, pueden contener sus propios archivos y directorios, etc.

El sistema de archivos proporcionó un único nivel de direccionamiento indirecto entre las aplicaciones y el disco, y el resultado fue que cada aplicación vio un archivo como una única secuencia contigua de bytes en el disco, aunque el sistema de archivos almacenara realmente el archivo en sectores no contiguos. El direccionamiento indirecto ha liberado a las aplicaciones de tener que realizar un seguimiento de la posición absoluta de los datos en un dispositivo de almacenamiento.

En la actualidad, prácticamente todas las API del sistema para la entrada y salida de archivos proporcionan aplicaciones para escribir información en un archivo plano. Las aplicaciones ven este archivo como un flujo de bytes único que puede crecer tan grande como sea necesario hasta que el disco esté lleno. Durante mucho tiempo, estas API han sido suficientes para que las aplicaciones almacenen su información persistente. Las aplicaciones han realizado importantes innovaciones en el modo en que se ocupan de una única secuencia de información para proporcionar características como el guardado "rápido" incremental.

Sin embargo, en un mundo de objetos de componentes, el almacenamiento de datos en un solo archivo plano ya no es eficaz. Del mismo modo que los sistemas de archivos surgieron de la necesidad de que varias aplicaciones compartan el mismo medio de almacenamiento, por lo que, ahora, los objetos de componente requieren un sistema que les permita compartir almacenamiento en el marco conceptual de un solo archivo. Aunque es posible almacenar los objetos independientes mediante el almacenamiento de archivo sin formato convencional, si uno de los objetos aumenta de tamaño, o si simplemente agrega otro objeto, es necesario cargar el archivo completo en la memoria, insertar el nuevo objeto y, a continuación, guardar el archivo completo. Este proceso puede llevar mucho tiempo.

La solución que proporciona COM es implementar un segundo nivel de direccionamiento indirecto: un sistema de archivos dentro de un archivo. El almacenamiento de archivo sin formato requiere que una secuencia de bytes contigua grande del disco se manipule a través de un único identificador de archivo con un único puntero de búsqueda. Por el contrario, el almacenamiento estructurado COM define cómo tratar una única entidad del sistema de archivos como una colección estructurada de dos tipos de objetos (almacenamientos y secuencias) que actúan como archivos y directorios.

 

 




