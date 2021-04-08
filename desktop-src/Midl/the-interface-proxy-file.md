---
title: El archivo de proxy de interfaz
description: El archivo de proxy de interfaz (U \_ p. c) es un archivo de c que contiene rutinas equivalentes a las de los archivos de código auxiliar de cliente y de código auxiliar de servidor de una interfaz de objeto (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL y COM MIDL, interfaces y archivos proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994415"
---
# <a name="the-interface-proxy-file"></a>El archivo de proxy de interfaz

El archivo de proxy de interfaz (U \_ p. c) es un archivo de c que contiene rutinas equivalentes a las de los archivos de código auxiliar de cliente y de código auxiliar de servidor de una interfaz de objeto (com). Este archivo contiene implementaciones de las rutinas suplentes para el cliente y el servidor en el modo en línea del compilador o datos equivalentes y thunks en los modos interpretados, así como otros datos de adherencia COM adecuados, como el proxy y las tablas auxiliares de código auxiliar.

El archivo de proxy de interfaz incluye las rutinas y los datos auxiliares solo para los métodos de las interfaces definidas en el archivo IDL actual. Para aclarar este comportamiento, se usa un ejemplo extendido en esta sección. Al compilar un archivo IDL con una interfaz como IFaceB que se hereda de IFaceA, se generan las rutinas y los datos auxiliares relacionados con IFaceB en el archivo proxy actual, mientras que la interfaz base IFaceA los datos y rutinas auxiliares relacionados se encuentran en el proxy generado a partir del archivo IDL que contiene la definición de IFaceA. El compilador genera todos los datos necesarios para identificar los suplentes de la interfaz base y delegarlos cuando sea necesario para admitir los métodos de IFaceA usados a través de la interfaz IFaceB.

Para cada método de una interfaz en el archivo IDL actual, el archivo del proxy contiene los dos métodos suplentes siguientes cuando se compilan en el modo mixto ([/os](-os.md)) y los datos de intérprete equivalentes cuando se compilan en el modo de intérprete ([/OI](-oi.md)).

-   El suplente del lado cliente, como el \_ proxy del método IFaceB \_ en este ejemplo.

    Este suplente del lado cliente es el punto de entrada virtual al que el cliente, por ejemplo, IFaceB:: Method, envía. Calcula las referencias de los argumentos de entrada en un formato de transmisión, transmite los argumentos de cálculo de referencias junto con información que identifica la interfaz y la operación y, a continuación, anula las referencias del valor devuelto y de los argumentos de salida cuando se devuelve la operación invocada.

-   El suplente del lado servidor, por ejemplo, el \_ código auxiliar del método IFaceB \_ .

    Este suplente del lado servidor es el punto de entrada virtual en el que se envía el tiempo de ejecución subyacente en el servidor para emular el cliente. Anula las referencias de los argumentos de entrada para replicar los datos de cliente, invoca la implementación del servidor de la función de interfaz y, a continuación, calcula las referencias y transmite el valor devuelto y los argumentos de salida al lado cliente.

El nombre predeterminado de un archivo proxy generado a partir de un archivo. idl es el archivo \_ p. c. Use el modificador del compilador MIDL de [**/proxy**](-proxy.md) para reemplazar el nombre predeterminado del archivo proxy de interfaz. Los modificadores [**/env**](-env.md) y [**/out**](-out.md) afectan a este archivo.

 

 




