---
title: Compilar gráficos de filtro para escribir archivos ASF (QASF)
description: Compilar gráficos de filtro para escribir archivos ASF (QASF)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows SDK de formato multimedia, creación de gráficos de filtro (QASF)
- Windows SDK de formato multimedia, DirectShow
- Windows SDK de formato multimedia, escritura de archivos ASF (QASF)
- Formato de sistemas avanzados (ASF), creación de gráficos de filtro (QASF)
- ASF (formato de sistemas avanzados), creación de gráficos de filtro (QASF)
- Formato de sistemas avanzados (ASF), escritura (QASF)
- ASF (formato de sistemas avanzados), escritura (QASF)
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, crear gráficos de filtro (QASF)
- DirectShow,escribir archivos ASF (QASF)
- Windows SDK de formato multimedia, QASF
- Formato de sistemas avanzados (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6128fb7578d829579aad7e8895be9db4d5a842aa785866253b553d4deb8b3b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055585"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a>Compilar gráficos de filtro para escribir archivos ASF (QASF)

Las aplicaciones basadas DirectShow suelen usar uno de los tres tipos básicos de gráficos de filtro al crear Windows contenido basado en medios:

-   Filtre los gráficos para convertir o transcodear contenido de otro formato en formato Windows multimedia.
-   Filtre los gráficos para insertar contenido que no Windows basado en multimedia (formatos de flujo nativos) en archivos ASF.
-   Filtre los gráficos para capturar datos en directo y codificar los datos inmediatamente Windows formato multimedia antes de guardarlos en el disco.

Cada tipo de gráfico de filtro se describe con más detalle en las secciones siguientes.



| Sección                                                                                                             | Descripción                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [Transcodificación de archivos (QASF)](transcoding-files--qasf.md)                                                             | Describe cómo crear gráficos de filtro de transcodificación de archivos.                                               |
| [Insertar formatos de flujo nativos en archivos ASF (QASF)](inserting-native-stream-formats-into-asf-files--qasf.md)   | Describe cómo colocar cualquier tipo de datos de audio o vídeo comprimidos o no comprimidos en un archivo ASF. |
| [Capturar directamente desde un dispositivo a un archivo ASF (QASF)](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | Describe cómo crear gráficos de filtro de captura que se emiten en un archivo ASF.                             |



 

 

 




