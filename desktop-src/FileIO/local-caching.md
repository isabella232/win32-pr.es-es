---
description: El almacenamiento en caché local de los datos es una técnica que se usa para agilizar el acceso a la red a los archivos de datos. Implica almacenar datos en caché en los clientes en lugar de en servidores cuando sea posible.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Almacenamiento en caché local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912853"
---
# <a name="local-caching"></a>Almacenamiento en caché local

El *almacenamiento en caché local* de los datos es una técnica que se usa para agilizar el acceso a la red a los archivos de datos. Implica almacenar datos en caché en los clientes en lugar de en servidores cuando sea posible.

El efecto del almacenamiento en caché local es que permite combinar varias operaciones de escritura en la misma región de un archivo en una operación de escritura a través de la red. El almacenamiento en caché local reduce el tráfico de red porque los datos se escriben una vez. Este almacenamiento en caché mejora el tiempo de respuesta aparente de las aplicaciones, ya que las aplicaciones no esperan a que se envíen los datos a través de la red al servidor.

El almacenamiento en caché local de los datos que se van a leer puede parecer más rápido gracias a la lectura de antemano. Un ejemplo sencillo es una aplicación que tiene acceso a datos secuencialmente, como el preprocesador del compilador. En tales casos, el nivel de red del sistema operativo Lee los datos a través de la red antes de que la aplicación solicite los datos. Idealmente, la red entrega los datos antes de que la aplicación los solicite del sistema de archivos, lo que da lugar a una respuesta casi instantánea. En la práctica, esto rara vez sucede, pero a menudo la lectura acelera las aplicaciones anticipando la solicitud siguiente.

El almacenamiento en caché local también puede ayudar a reducir el tráfico de red mediante la lectura de una parte de un archivo a través de la red una vez y su mantenimiento en la caché local. Operaciones de lectura posteriores en esa parte por la aplicación leída desde la memoria caché local.

Un tipo de aplicación que se puede beneficiar del almacenamiento en caché local son los archivos por lotes. Los procesadores de comandos leen y ejecutan un archivo por lotes una línea a la vez. En cada línea, el procesador de comandos abre el archivo, busca en el principio de la línea, lee tanto como sea necesario, cierra el archivo y, a continuación, ejecuta la línea. Cada línea tiene como resultado una gran cantidad de tráfico de red. El tráfico de red se puede reducir considerablemente almacenando en caché todo el archivo por lotes en un cliente.

El almacenamiento en caché local también ayuda con otro problema asociado a las redes, especialmente a las redes que realizan el trabajo a través de módems y otras canalizaciones delgadas: tiempo de respuesta lento. Los usuarios no quieren esperar mientras los datos se recuperan a través de la red, se modifican y se escriben de nuevo. Con la lectura previa y el almacenamiento en caché de escritura, a menudo parece que estas funciones funcionan mucho más rápido de lo que hacen realmente.

Un riesgo de almacenamiento en caché local es que los datos escritos solo tienen tanta integridad como el cliente, siempre y cuando los datos se almacenen en la memoria caché del cliente. En general, los datos almacenados en caché localmente se deben vaciar en el servidor lo antes posible. Con los sistemas operativos modernos y la compatibilidad de hardware, como las fuentes de alimentación ininterrumpidas, se reduce el riesgo de perder los datos almacenados en caché localmente. Pero el riesgo todavía existe y debe considerar el equilibrio entre la integridad de los datos y la velocidad de respuesta aparente y el equilibrio entre la integridad de los datos y el tráfico de red reducido.

 

 



