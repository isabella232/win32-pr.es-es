---
title: Receptores
description: Receptores
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows SDK de formato multimedia, receptores
- Windows SDK de formato multimedia, receptores de archivos
- Formato de sistemas avanzados (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- Formato de sistemas avanzados (ASF), receptores de archivos
- ASF (formato de sistemas avanzados), receptores de archivos
- Windows SDK de formato multimedia, receptores de red
- Windows SDK de formato multimedia, receptores de inserción
- Formato de sistemas avanzados (ASF), receptores de red
- ASF (formato de sistemas avanzados), receptores de red
- Formato de sistemas avanzados (ASF), receptores de inserción
- ASF (formato de sistemas avanzados), receptores de inserción
- sinks,about
- receptores de archivos, acerca de
- receptores de red
- receptores de inserción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb72479a231c3db508efcea7db54528c0b1bf9635afba8b842a4c23add0456cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807905"
---
# <a name="sinks"></a>Receptores

El objeto de escritor del SDK Windows Media Format entrega contenido procesado a los receptores. Cada receptor es un objeto que entrega datos. El punto de entrega depende del tipo de receptor. Hay tres tipos de receptores: receptores de archivos, receptores de red y receptores de inserción.

## <a name="file-sinks"></a>Receptores de archivos

Los receptores de archivos escriben contenido de ASF en un archivo en una unidad local o de red. Cuando se usa el objeto de escritor para escribir un archivo sin agregar explícitamente un receptor de archivos, el escritor creará uno automáticamente con el nombre que pase a [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). Puede asignar varios receptores de archivos a un objeto de escritor para escribir el contenido en varios archivos a la vez.

Mediante el uso de un receptor de archivos, puede controlar muchos aspectos del archivo. Las siguientes características están disponibles a través de un receptor de archivos.

-   Supervisión de estadísticas de archivos. Puede supervisar el tamaño y la duración del archivo a medida que se crea.
-   Creación parcial de archivos de contenido. Los receptores de archivos se pueden configurar para empezar a escribir contenido en un momento específico y terminar la escritura en un momento específico. Esto le permite crear varios archivos que contienen secciones diferentes del mismo contenido en el mismo paso de escritura.

## <a name="network-sinks"></a>Receptores de red

Receptores de red difunden contenido a una dirección de red. Los clientes de lectura pueden conectarse a la dirección para recibir la difusión.

## <a name="push-sinks"></a>Receptores de inserción

Los receptores de inserción entregan contenido del escritor a un servidor que ejecuta Servicios de Windows Media. Los receptores de inserción se usan normalmente en escenarios en los que un equipo codifica contenido en directo y lo entrega a uno o varios servidores para una distribución amplia. El uso de un receptor de inserción permite dedicar equipos a tareas específicas, lo que ahorra ancho de banda y potencia de procesamiento en cada servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




