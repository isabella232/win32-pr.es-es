---
title: El archivo de proxy de interfaz
description: El archivo proxy de interfaz (U p.c) es un archivo C que contiene rutinas equivalentes a las del código auxiliar de cliente y los archivos de código auxiliar del servidor de una interfaz \_ de objeto (COM).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL y COM MIDL, interfaces, archivos proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159355"
---
# <a name="the-interface-proxy-file"></a>El archivo de proxy de interfaz

El archivo proxy de interfaz (U p.c) es un archivo C que contiene rutinas equivalentes a las del código auxiliar de cliente y los archivos de código auxiliar del servidor de una interfaz \_ de objeto (COM). Este archivo contiene implementaciones de las rutinas suplentes para cliente y servidor en el modo en línea del compilador o datos equivalentes y thunks en los modos interpretados, así como otros datos de adherencia COM adecuados, como el proxy y las Vtables de código auxiliar.

El archivo proxy de interfaz incluye las rutinas y los datos auxiliares solo para los métodos de las interfaces definidas en el archivo IDL actual. Para aclarar este comportamiento, se usa un ejemplo extendido en esta sección. Al compilar un archivo IDL con una interfaz como IFaceB que hereda de IFaceA, se generan rutinas y datos auxiliares relacionados con IFaceB en el archivo proxy actual, mientras que la interfaz base IFaceA se encuentra en el proxy generado a partir del archivo IDL que contiene la definición de IFaceA. El compilador genera todos los datos necesarios para identificar los suplentes de la interfaz base y delegarlos cuando sea necesario para admitir los métodos IFaceA usados a través de la interfaz IFaceB.

Para cada método de una interfaz en el archivo IDL actual, el archivo proxy contiene los dos métodos suplentes siguientes cuando se compilan en el modo mixto ([/Os](-os.md)) y los datos de intérprete equivalentes cuando se compilan en el modo de intérprete ([/Oi](-oi.md)).

-   El suplente del lado cliente, como el proxy del método IFaceB \_ \_ en este ejemplo.

    Este suplente del lado cliente es el punto de entrada virtual al que envía el cliente, por ejemplo IFaceB::Method. Serializa los argumentos de entrada en un formato transmitible, transmite los argumentos serializados junto con la información que identifica la interfaz y la operación y, a continuación, desmarque el valor devuelto y los argumentos de salida cuando se devuelve la operación invocada.

-   El suplente del lado servidor, por ejemplo, IFaceB \_ Method \_ Stub .

    Este suplente del lado servidor es el punto de entrada virtual al que el tiempo de ejecución subyacente envía en el servidor para emular el cliente. Desmarque los argumentos de entrada para replicar los datos de cliente, invoca la implementación del servidor de la función de interfaz y, a continuación, serializa y transmite el valor devuelto y los argumentos de salida al lado cliente.

El nombre predeterminado de un archivo proxy generado a partir de un archivo file.idl es el archivo p.c.Use el modificador del compilador /proxy MIDL para invalidar el nombre predeterminado del archivo proxy de \_ interfaz. [](-proxy.md) Los [**modificadores /env**](-env.md) [**y /out**](-out.md) afectan a este archivo.

 

 




