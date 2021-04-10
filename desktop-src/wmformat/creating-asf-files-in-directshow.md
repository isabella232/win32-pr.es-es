---
title: Crear archivos ASF en DirectShow (Windows Media Format 11 SDK)
description: Crear archivos ASF en DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- SDK de Windows Media Format, crear archivos ASF en DirectShow
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- Advanced Systems Format (ASF), crear en DirectShow
- ASF (formato de sistemas avanzados), crear en DirectShow
- DirectShow, crear archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149785"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Crear archivos ASF en DirectShow (Windows Media Format 11 SDK)

Puede usar DirectShow para crear archivos ASF directamente desde orígenes de captura, como videocámaras DV, o para transcodificar otros archivos en el formato de Windows Media. En cualquier escenario, las aplicaciones crean gráficos de filtro que incluyen el filtro de [escritor ASF de WM](wm-asf-writer-filter.md) como representador.

El escritor ASF de WM proporciona un contenedor parcial para el SDK de Windows Media Format. Las aplicaciones pueden usar la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro para pasar un perfil del sistema (versiones 4, 7 u 8), o bien usar el SDK de Windows Media Format directamente para crear un perfil personalizado y pasarlo al filtro. Para agregar metadatos y otra información de encabezado, la aplicación usa la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , que se puede obtener del filtro. Una vez configurados el perfil y los metadatos, la aplicación puede simplemente ejecutar el gráfico de filtro. Internamente, el filtro usa el SDK de Windows Media Format para escribir el archivo. El filtro controla todos los detalles de la sincronización de audio y vídeo, que de otro modo sería responsabilidad de la aplicación.

Este proceso se explica con más detalle en las secciones siguientes.



| Sección                                                                                                           | Descripción                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configuración del escritor ASF de WM (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Describe cómo configurar el filtro del escritor ASF de WM.                                   |
| [Generar gráficos de filtro para escribir archivos ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Describe cómo crear gráficos de captura y de transcodificación de archivos.                           |
| [Configuración de perfiles y otras propiedades de archivo (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Describe cómo realizar diversas tareas de configuración de archivos ASF mediante el escritor ASF de WM. |



 

 

 
