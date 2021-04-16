---
description: Acerca de las topologías
ms.assetid: 4f69b099-0ca7-4ea6-8412-0f1ea02e1600
title: Acerca de las topologías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35008d839e8054554370039dd13297ae7a1f0b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562295"
---
# <a name="about-topologies"></a>Acerca de las topologías

Una topología es un objeto que representa cómo fluyen los datos en la canalización. Una aplicación crea una topología para describir la ruta de acceso que cada flujo toma del origen de medios a un receptor de medios. La aplicación pasa la topología a la sesión multimedia y la sesión multimedia utiliza la topología para controlar el flujo de datos.

Los componentes de procesamiento de datos de la canalización (orígenes multimedia, transformaciones y receptores multimedia) se representan en la topología como *nodos*. El flujo de datos de un componente a otro se representa mediante una conexión entre los nodos. Se definen los siguientes tipos de nodo:

-   Nodo de origen: representa una secuencia de medios en un origen de multimedia.
-   Nodo de transformación: representa una transformación de Media Foundation (MFT).
-   Nodo de salida: representa un receptor de flujo en un receptor de multimedia.
-   Tee node: representa una bifurcación en la secuencia. Los nodos Tee son una excepción a la regla de que un nodo representa un objeto de canalización. A diferencia de otros tipos de nodo, el nodo Tee simplemente dirige el flujo de datos.

Una topología funcional debe contener al menos un nodo de origen conectado a un nodo de salida, posiblemente a través de uno o varios nodos de transformación. Por ejemplo, en el diagrama siguiente se muestra una topología simple con una secuencia.

![diagrama que muestra una topología con un flujo.](images/topology01.png)

En la reproducción de archivos, el nodo de transformación podría representar un descodificador y el nodo de salida representaría el representador de audio o vídeo. En cuanto a la codificación de archivos, el nodo de transformación representaría un codificador y el nodo de salida representaría un receptor de archivo, como el receptor de archivos ASF.

Si dos nodos están conectados, el nodo que produce los datos se denomina nodo *ascendente* y el nodo que recibe los datos se denomina nodo de *nivel inferior* . Por ejemplo, en el diagrama anterior, el nodo de origen se encuentra en el flujo ascendente del nodo de transformación.

En un par de nodos conectados, el punto de conexión en el nodo de nivel superior se denomina *salida*. El punto de conexión en el nodo de nivel inferior se denomina *entrada*. En el diagrama siguiente se muestra un par de nodos con sus puntos de conexión y el flujo de datos entre ellos. Los puntos de conexión no se representan como objetos independientes en la topología. Se especifican mediante el valor de índice en el objeto node.

![diagrama que muestra dos nodos conectados.](images/topology04.png)

Un nodo de origen no puede tener ninguna entrada. Por lo tanto, no puede haber ningún nodo de nivel superior desde un nodo de origen. De forma similar, un nodo de salida no puede tener salidas y no puede haber ningún nodo de nivel inferior desde un nodo de salida. Una cadena de nodos de un nodo de origen a un nodo de salida se denomina *rama* de la topología. En el primer diagrama de este tema se muestra una topología con una sola rama. Por lo general, hay una rama por secuencia. Para reproducir un archivo con una secuencia de audio y una secuencia de vídeo, por ejemplo, se requiere una topología con dos bifurcaciones.

## <a name="partial-topologies"></a>Topologías parciales

Una topología completa *o completa* contiene un nodo para cada objeto de canalización que se necesita. Sin embargo, la aplicación no siempre tiene que crear una topología completa. En su lugar, crea una topología *parcial* que omite uno o varios nodos de transformación.

La sesión multimedia completa la topología mediante un objeto denominado *cargador de topología*. El cargador de topología convierte las topologías parciales en topologías completas insertando las transformaciones necesarias. El proceso de conversión se denomina *resolver* la topología.

Por ejemplo, para reproducir una secuencia de audio codificada, la topología debe tener un descodificador entre los nodos de origen y de salida. La aplicación crea una topología parcial que conecta el nodo de origen directamente con el nodo de salida, sin el descodificador. El cargador de topología examina los formatos de flujo, encuentra el descodificador correcto e inserta un nodo de transformación en la topología.

En el diagrama siguiente se muestra la topología parcial creada por la aplicación.

![diagrama que muestra una parcial con un nodo de origen y un nodo de salida.](images/topology02.png)

En el diagrama siguiente se muestra la topología completa después de que el cargador de topología la resuelva. En este ejemplo, el cargador de topología ha insertado un nodo de transformación para el descodificador.

![diagrama que muestra una topología completa.](images/topology03.png)

En la versión actual de Media Foundation, el cargador de topología admite topologías para la reproducción. En cuanto a la codificación de archivos y otros escenarios, la aplicación debe construir una topología completa.

Las aplicaciones también pueden crear el cargador de topología y usarlo directamente. Por ejemplo, puede usar el cargador de topología para resolver una topología parcial y, a continuación, modificar la topología completa antes de asignarla a la sesión multimedia. Para crear el cargador de topología, llame a [**MFCreateTopoLoader**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopoloader).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



