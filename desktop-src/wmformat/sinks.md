---
title: Receptores
description: Receptores
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- SDK de Windows Media Format, receptores
- SDK de Windows Media Format, receptores de archivo
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- Formato de sistemas avanzados (ASF), receptores de archivo
- ASF (formato de sistemas avanzados), receptores de archivo
- SDK de Windows Media Format, receptores de red
- SDK de Windows Media Format, receptores de envío
- Advanced Systems Format (ASF), receptores de red
- ASF (formato de sistemas avanzados), receptores de red
- Advanced Systems Format (ASF), receptores de envío
- ASF (formato de sistemas avanzados), receptores de inserciones
- receptores, acerca de
- receptores de archivos, acerca de
- receptores de red
- receptores de extracción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077340"
---
# <a name="sinks"></a>Receptores

El objeto escritor del SDK de Windows Media Format entrega el contenido procesado a los receptores. Cada receptor es un objeto que proporciona datos. El punto de entrega depende del tipo de receptor. Hay tres tipos de receptores: receptores de archivos, receptores de red y receptores de envío.

## <a name="file-sinks"></a>Receptores de archivo

Los receptores de archivos escriben contenido ASF en un archivo de una unidad local o de red. Cuando se usa el objeto de escritor para escribir un archivo sin agregar explícitamente un receptor de archivos, el escritor creará uno para el usuario con el nombre que se pasa a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). Puede asignar varios receptores de archivo a un objeto de escritura para escribir el contenido en varios archivos a la vez.

Mediante el uso de un receptor de archivos, puede controlar muchos aspectos del archivo. Las siguientes características están disponibles a través de un receptor de archivos.

-   Supervisión de estadísticas de archivo. Puede supervisar el tamaño y la duración del archivo a medida que se crea.
-   Creación parcial de archivos de contenido. Los receptores de archivos pueden configurarse para comenzar a escribir contenido en un momento específico y finalizar la escritura en un momento determinado. Esto le permite crear varios archivos que contienen diferentes secciones del mismo contenido en el mismo paso de escritura.

## <a name="network-sinks"></a>Receptores de red

Los receptores de red retransmiten contenido a una dirección de red. La lectura de clientes puede conectarse a la dirección para recibir la difusión.

## <a name="push-sinks"></a>Receptores de extracción

Los receptores de extracción entregan contenido del escritor a un servidor que ejecuta Windows Media Services. Los receptores de envío se usan normalmente en escenarios en los que un equipo codifica el contenido en directo y lo entrega a uno o varios servidores para una distribución amplia. El uso de un receptor de inserciones le permite dedicar equipos a tareas específicas, lo que ahorra ancho de banda y capacidad de procesamiento en cada servidor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de escritura de archivos**](file-writing-features.md)
</dt> <dt>

[**Trabajar con receptores de escritor**](working-with-writer-sinks.md)
</dt> </dl>

 

 




