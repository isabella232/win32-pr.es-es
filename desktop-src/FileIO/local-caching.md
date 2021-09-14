---
description: El almacenamiento en caché local de datos es una técnica que se usa para acelerar el acceso de red a los archivos de datos. Implica almacenar datos en caché en clientes en lugar de en servidores cuando sea posible.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Almacenamiento en caché local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069920"
---
# <a name="local-caching"></a>Almacenamiento en caché local

*El almacenamiento en caché local* de datos es una técnica que se usa para acelerar el acceso de red a los archivos de datos. Implica almacenar datos en caché en clientes en lugar de en servidores cuando sea posible.

El efecto del almacenamiento en caché local es que permite combinar varias operaciones de escritura en la misma región de un archivo en una operación de escritura a través de la red. El almacenamiento en caché local reduce el tráfico de red porque los datos se escriben una vez. Este almacenamiento en caché mejora el tiempo de respuesta aparente de las aplicaciones porque las aplicaciones no esperan a que los datos se envíen a través de la red al servidor.

El almacenamiento en caché local de los datos que se van a leer puede parecer que acelera las cosas mediante la lectura con antelación. Un ejemplo sencillo es una aplicación que accede a los datos secuencialmente, como el preprocesador de un compilador. En tales casos, la capa de red del sistema operativo lee los datos a través de la red antes de que la aplicación solicite los datos. Idealmente, la red entrega los datos antes de que la aplicación los solicite desde el sistema de archivos, lo que da lugar a una respuesta casi instantánea. En la práctica, esto rara vez ocurre, pero a menudo la lectura anticipada acelera las aplicaciones al anticiparse a la siguiente solicitud.

El almacenamiento en caché local también puede ayudar a reducir el tráfico de red mediante la lectura de una parte de un archivo a través de la red una vez y, a continuación, mantenerlo en la caché local. Operaciones de lectura posteriores en esa parte por parte de la aplicación leídas desde la memoria caché local.

Un tipo de aplicación que puede beneficiarse del almacenamiento en caché local son los archivos por lotes. Los procesadores de comandos leen y ejecutan un archivo por lotes línea a línea. Para cada línea, el procesador de comandos abre el archivo, busca al principio de la línea, lee todo lo que necesita, cierra el archivo y, a continuación, ejecuta la línea. Cada línea da como resultado una gran cantidad de tráfico de red. El tráfico de red se puede reducir considerablemente almacenando en caché todo el archivo por lotes en un cliente.

El almacenamiento en caché local también ayuda con otro problema asociado a las redes, especialmente las redes que realizan el trabajo a través de módems y otras canalizaciones finas: tiempo de respuesta lento. Los usuarios no quieren esperar mientras se recuperan los datos a través de la red, se modifican y, a continuación, se escriben de nuevo. Con la lectura por adelantado y el almacenamiento en caché de escritura, a menudo parece que estas funciones funcionan mucho más rápido de lo que realmente hacen.

Un riesgo del almacenamiento en caché local es que los datos escritos solo tienen tanta integridad como el propio cliente mientras los datos se almacenen en caché en el cliente. En general, los datos almacenados localmente en caché deben vaciarse en el servidor tan pronto como sea posible. Con sistemas operativos modernos y compatibilidad con hardware, como fuentes de alimentación ininterrumpidas, se reduce el riesgo de perder datos almacenados en caché localmente. Pero el riesgo sigue existiendo y debe tener en cuenta el equilibrio entre la integridad de los datos y la velocidad de respuesta aparente, así como el equilibrio entre la integridad de los datos y el tráfico de red reducido.

 

 



