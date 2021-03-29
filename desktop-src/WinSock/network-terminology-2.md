---
description: Las métricas se utilizan para medir aspectos del rendimiento de la red y del protocolo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminología de red (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809715"
---
# <a name="network-terminology-windows-sockets-2"></a>Terminología de red (Windows Sockets 2)

Las métricas se utilizan para medir aspectos del rendimiento de la red y del protocolo. Los valores de estas métricas en varios escenarios indican el nivel de rendimiento de una aplicación de red. En esta sección se definen los términos y las métricas usados en todo el sector para medir el rendimiento de las aplicaciones de red. Estos términos se usan en el resto de esta guía.

-   Tiempo de ida y vuelta (RTT)

    Tiempo, en milisegundos, que tarda una solicitud en realizar un recorrido desde un equipo de origen a un equipo de destino y viceversa. Los valores menores indican un mejor rendimiento. Los tiempos de rutas de acceso hacia delante y devueltos no son necesariamente iguales.

    Los valores de RTT se ven afectados por la infraestructura de red, la distancia entre los nodos, las condiciones de la red y el tamaño de los paquetes. El tamaño de paquete, la congestión y la carga compresión afectan al RTT cuando se mide en vínculos de baja velocidad, como conexiones de acceso telefónico. Otros factores afectan a RTT, incluida la corrección de errores de reenvío y la compresión de datos, que introducen búferes y colas que aumentan el RTT y, por tanto, reducen el rendimiento.

-   Goodput

    Medida de datos de aplicación útiles procesados correctamente por el receptor, en bits por segundo. Goodput habilita la medición del rendimiento eficaz o útil e incluye solo los datos de la aplicación; Los encabezados de paquetes, protocolos y medios se consideran una sobrecarga y no forman parte de goodput.

-   Sobrecarga de protocolo

    Bytes que no son de aplicación, incluidos tramas de protocolo y multimedia, divididos por el número total de bytes transmitidos. El valor se expresa como un porcentaje. Los valores más altos indican un rendimiento más bajo.

    La sobrecarga se calcula en ambas direcciones de esta guía, pero se puede calcular para cada dirección por separado.

-   Bandwidth-Delay producto

    Producto del ancho de banda de bits por segundo de la red y el RTT (en segundos). Este valor equivale al número de bits que se tarda en rellenar el ancho de banda de red disponible. Cuando el valor del producto de retraso de ancho de banda es alto, la pila TCP/IP debe administrar grandes cantidades de datos no confirmados para que la canalización esté completa. El producto de retraso de ancho de banda es una métrica de extremo a extremo de la clave para las aplicaciones de streaming.

 

 



