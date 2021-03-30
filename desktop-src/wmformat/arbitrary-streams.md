---
title: Flujos arbitrarios
description: Flujos arbitrarios
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- SDK de Windows Media Format, secuencias arbitrarias
- Advanced Systems Format (ASF), streams arbitrarios
- ASF (formato de sistemas avanzados), secuencias arbitrarias
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- flujos arbitrarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773405"
---
# <a name="arbitrary-streams"></a>Flujos arbitrarios

Además de las secuencias de audio y vídeo, y las secuencias de imágenes, un archivo ASF puede alojar secuencias que contengan una variedad de datos. Los objetos del SDK de Windows Media Format proporcionan compatibilidad con secuencias de scripts, secuencias de transferencia de archivos, secuencias web y flujos de datos arbitrarios. Todos estos tipos de flujo son arbitrarios, lo que significa que el objeto de lectura no realiza ninguna validación de datos. Al incluir secuencias de estos tipos en los archivos, asegúrese de que la aplicación de lectura realiza la validación o la comprobación de datos para asegurarse de que el contenido no se ha dañado o se ha alterado intencionadamente por un tercero malintencionado.

Aunque los objetos de este SDK no comprueban ni validan datos en flujos arbitrarios, se admiten de forma nativa varios tipos de secuencias arbitrarias. En la tabla siguiente se enumeran los tipos de secuencia arbitrarios predefinidos. También se admiten secuencias de script, pero se tratan por separado en la sección [comandos de script](script-commands.md) . Para obtener más información sobre la creación de tipos personalizados, vea [flujos de datos arbitrarios personalizados](custom-arbitrary-data-streams.md).



| Tipo arbitrario                   | Descripción                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Secuencias de texto](text-streams.md) | Contienen cadenas de texto.                                             |
| [Secuencias de archivo](file-streams.md) | Contener uno o más archivos de datos.                                   |
| [Secuencias Web](web-streams.md)   | Contienen archivos de datos equivalentes a la versión almacenada en caché de las páginas Web. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Secuencias de audio y vídeo**](audio-and-video-streams.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




