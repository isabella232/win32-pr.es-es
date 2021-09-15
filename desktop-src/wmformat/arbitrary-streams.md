---
title: Datos arbitrarios Secuencias
description: Datos arbitrarios Secuencias
ms.assetid: 81fd3b07-7cf2-4013-97ed-9718142ca4c3
keywords:
- Windows SDK de formato multimedia, secuencias arbitrarias
- Formato de sistemas avanzados (ASF), secuencias arbitrarias
- ASF (formato de sistemas avanzados), secuencias arbitrarias
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- secuencias arbitrarias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe28a3b30e0f711c69998b78c81fc1e745fe6360
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570257"
---
# <a name="arbitrary-streams"></a>Datos arbitrarios Secuencias

Además de las secuencias de audio y vídeo y las secuencias de imagen, un archivo ASF puede dar cabida a secuencias que contienen una variedad de datos. Los objetos del SDK Windows Media Format proporcionan compatibilidad con secuencias de script, flujos de transferencia de archivos, flujos web y flujos de datos arbitrarios. Todos estos tipos de flujo son arbitrarios, lo que significa que el objeto de lectura no realiza ninguna validación de datos. Cuando incluya secuencias de estos tipos en los archivos, asegúrese de que la aplicación de lectura realiza la validación o la comprobación de datos para asegurarse de que un tercero malintencionado no ha dañado o dañado intencionadamente el contenido.

Aunque los objetos de este SDK no comprueban ni validan datos en secuencias arbitrarias, se admiten de forma nativa varios tipos de secuencias arbitrarias. En la tabla siguiente se enumeran los tipos de secuencia arbitrarios predefinidos. También se admiten secuencias de scripts, pero se analizan por separado en la [sección Comandos de](script-commands.md) script. Para obtener más información sobre cómo crear tipos personalizados, vea [Custom Arbitrary Data Secuencias](custom-arbitrary-data-streams.md).



| Tipo arbitrario                   | Descripción                                                       |
|----------------------------------|-------------------------------------------------------------------|
| [Secuencias de texto](text-streams.md) | Contiene cadenas de texto.                                             |
| [Archivo Secuencias](file-streams.md) | Contenga uno o varios archivos de datos.                                   |
| [Web Secuencias](web-streams.md)   | Contienen archivos de datos equivalentes a la versión almacenada en caché de las páginas web. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Audio y vídeo Secuencias**](audio-and-video-streams.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> </dl>

 

 




