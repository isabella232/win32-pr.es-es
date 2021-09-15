---
description: Las métricas se usan para medir aspectos del rendimiento de la red y del protocolo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminología de red (Windows sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474519"
---
# <a name="network-terminology-windows-sockets-2"></a>Terminología de red (Windows sockets 2)

Las métricas se usan para medir aspectos del rendimiento de la red y del protocolo. Los valores de estas métricas en varios escenarios indican el nivel de rendimiento de una aplicación de red. En esta sección se definen los términos y las métricas usados en todo el sector para medir el rendimiento de las aplicaciones de red. Estos términos se usan en el resto de esta guía.

-   Tiempo de ida y vuelta (RTT)

    Tiempo, en milisegundos, para que una solicitud realice un viaje desde un equipo de origen a un equipo de destino y vuelva de nuevo. Los valores más bajos indican un mejor rendimiento. Los tiempos de las rutas de acceso de reenvío y de retorno no son necesariamente iguales.

    Los valores RTT se ven afectados por la infraestructura de red, la distancia entre los nodos, las condiciones de red y el tamaño del paquete. El tamaño de los paquetes, la congestión y la compresión de carga afectan a RTT cuando se mide en vínculos lentos, como las conexiones de acceso telefónico. Otros factores afectan a RTT, incluida la corrección de errores hacia delante y la compresión de datos, que introducen búferes y colas que aumentan RTT y, por tanto, reducen el rendimiento.

-   Goodput

    Medida de datos útiles de la aplicación procesados correctamente por el receptor, en bits por segundo. Goodput permite medir el rendimiento eficaz o útil e incluye solo los datos de la aplicación. Los encabezados de paquete, protocolo y multimedia se consideran sobrecarga y no forman parte de goodput.

-   Sobrecarga del protocolo

    Bytes no de aplicación, incluidos el protocolo y el marco multimedia, divididos por el número total de bytes transmitidos. El valor se expresa como un porcentaje. Los valores más altos indican un rendimiento más bajo.

    La sobrecarga se calcula para ambas direcciones en esta guía, pero se puede calcular para cada dirección por separado.

-   Bandwidth-Delay product

    Producto del ancho de banda de bits por segundo de la red y el RTT (en segundos). Este valor equivale al número de bits que se necesitan para rellenar el ancho de banda de red disponible. Cuando el valor del producto de retraso de ancho de banda es alto, la pila TCP/IP debe controlar grandes cantidades de datos no reconocidos para mantener la canalización llena. El producto de retraso de ancho de banda es una métrica de un extremo a otro clave para las aplicaciones de streaming.

 

 



