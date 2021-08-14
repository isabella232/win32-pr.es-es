---
description: Creación de una topología de reproducción con TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Creación de una topología de reproducción con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a71ae353c11108fe7c844d8ddd6441e652e007646b91f44c6fe2b480a22a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035433"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Creación de una topología de reproducción con TopoEdit

TopoEdit puede compilar una topología de reproducción para un archivo multimedia local agregando y conectando automáticamente los nodos de origen, transformación y salida. TopoEdit no resuelve automáticamente la topología. Para reproducir la topología, resálala y, a continuación, use los controles de transporte.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>Para compilar y reproducir una topología para un archivo multimedia

1.  En el menú **Archivo** , haga clic en **Representar archivo**.

    Se abrirá el cuadro **de diálogo Seleccionar origen** multimedia.

2.  Vaya a la carpeta donde se encuentra el archivo multimedia.
3.  En el **campo Nombre de archivo:** , escriba el nombre del archivo.
4.  Haga clic en **Abrir**.

    El **panel Topología muestra** la topología conectada. Internamente, TopoEdit realiza las siguientes tareas:

    -   Enumera las secuencias del archivo multimedia y crea los nodos de origen.
    -   En función del tipo de medio de los nodos de origen, agrega nodos de transformación, como descodificadores.
    -   Agrega el receptor Streaming Audio Renderer (SAR) para la secuencia de audio y el receptor de representador de vídeo mejorado (EVR) para la secuencia de vídeo.
    -   Conecta las entradas del nodo y las salidas del nodo.

5.  En el **menú Topología,** haga clic **en Resolver topología.**
6.  Haga clic en **el botón** Reproducir de la barra de herramientas para reproducir la topología. En la imagen siguiente se muestra el **botón Reproducir** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de reproducción en TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



