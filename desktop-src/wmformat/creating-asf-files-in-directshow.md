---
title: Crear archivos ASF en DirectShow (Windows SDK de formato multimedia 11)
description: Obtenga información sobre cómo crear archivos ASF DirectShow mediante el SDK Windows Media Format 11. ASF es un formato de contenedor que puede contener cualquier tipo de datos.
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows SDK de formato multimedia, creación de archivos ASF en DirectShow
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- Formato de sistemas avanzados (ASF), crear en DirectShow
- ASF (formato de sistemas avanzados), crear en DirectShow
- DirectShow, crear archivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e06b6deb6dc9f07115f8143309d32dcf4a58a0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466721"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a>Crear archivos ASF en DirectShow (Windows SDK de formato multimedia 11)

Puede usar DirectShow para crear archivos ASF directamente desde orígenes de captura, como cámaras de vídeo DV, o para transcodificar otros archivos en Windows Media Format. En cualquier escenario, las aplicaciones crean gráficos de filtro que incluyen el filtro [WM ASF Writer](wm-asf-writer-filter.md) como representador.

WM ASF Writer proporciona un contenedor parcial para el SDK Windows Media Format. Las aplicaciones pueden usar la interfaz [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) del filtro para pasar un perfil del sistema (versiones 4, 7 o 8) o usar el SDK de formato multimedia de Windows directamente para crear un perfil personalizado que se pase al filtro. Para agregar metadatos y otra información de encabezado, la aplicación usa la [**interfaz IWMHeaderInfo,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) que se puede obtener del filtro. Una vez configurados el perfil y los metadatos, la aplicación puede ejecutar simplemente el gráfico de filtros. Internamente, el filtro usa Windows SDK de formato multimedia para escribir el archivo. El filtro controla todos los detalles de sincronización de audio y vídeo, que de lo contrario serían responsabilidad de la aplicación.

Este proceso se explica con más detalle en las secciones siguientes.



| Sección                                                                                                           | Descripción                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [Configuración de WM ASF Writer (QASF)](configuring-the-wm-asf-writer--qasf.md)                                   | Describe cómo configurar el filtro WM ASF Writer.                                   |
| [Creación de gráficos de filtro para escribir archivos ASF (QASF)](building-filter-graphs-to-write-asf-files--qasf.md)           | Describe cómo crear gráficos de transcodificación y captura de archivos.                           |
| [Configuración de perfiles y otras propiedades de archivo (QASF)](configuring-profiles-and-other-file-properties--qasf.md) | Describe cómo realizar varias tareas de configuración de archivos de ASF mediante WM ASF Writer. |



 

 

 
