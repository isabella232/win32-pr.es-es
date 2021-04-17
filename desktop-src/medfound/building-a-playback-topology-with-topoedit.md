---
description: Creación de una topología de reproducción con TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Creación de una topología de reproducción con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f942984b3ba56ef1288566cee80e7d30026de155
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "105697900"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Creación de una topología de reproducción con TopoEdit

TopoEdit puede crear una topología de reproducción para un archivo multimedia local mediante la adición y conexión automática de los nodos de origen, transformación y salida. TopoEdit no resuelve automáticamente la topología. Para reproducir la topología, resuélvalos y, a continuación, use los controles de transporte.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>Para compilar y reproducir una topología para un archivo multimedia

1.  En el menú **archivo** , haga clic en **archivo de representación**.

    Se abrirá el cuadro de diálogo **Seleccionar origen de medios** .

2.  Navegue hasta la carpeta donde se encuentra el archivo multimedia.
3.  En el campo **nombre de archivo:** , escriba el nombre del archivo.
4.  Haga clic en **Abrir**.

    En el **Panel de topología** se muestra la topología conectada. Internamente, TopoEdit realiza las siguientes tareas:

    -   Enumera las secuencias del archivo multimedia y crea los nodos de origen.
    -   En función del tipo de medio de los nodos de origen, agrega nodos de transformación, como descodificadores.
    -   Agrega el receptor del representador de audio de streaming (SAR) para el flujo de audio y el receptor de representador de vídeo mejorado (EVR) para la secuencia de vídeo.
    -   Conecta las entradas de nodo y las salidas de nodo.

5.  En el menú **topología** , haga clic en **resolver topología**.
6.  Haga clic en el botón **reproducir** de la barra de herramientas para reproducir la topología. En la imagen siguiente se muestra el botón **reproducir** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles de reproducción en TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



