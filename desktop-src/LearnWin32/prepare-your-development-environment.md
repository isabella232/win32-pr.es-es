---
title: Preparación del entorno de desarrollo
description: Preparación del entorno de desarrollo
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: 8245326ba0d7862836336cf050eb3abf1873139873bde8b9bab238ff5a738942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896975"
---
# <a name="prepare-your-development-environment"></a>Preparación del entorno de desarrollo

Para escribir un Windows en C o C++, debe instalar el Kit de desarrollo de software (SDK) de Microsoft Windows o Microsoft Visual Studio. El SDK Windows contiene los encabezados y bibliotecas necesarios para compilar y vincular la aplicación. El SDK Windows también contiene herramientas de línea de comandos para compilar Windows, incluidos el compilador y el vinculador de Visual C++. Aunque puede compilar y compilar Windows con las herramientas de línea de comandos, se recomienda usar Microsoft Visual Studio. Puede descargar una descarga gratuita de Visual Studio Community o pruebas gratuitas de otras versiones de Visual Studio [aquí.](https://visualstudio.microsoft.com/downloads/)

Cada versión del SDK de Windows tiene como destino la versión más reciente de Windows así como varias versiones anteriores. Las notas de la versión enumeran las plataformas específicas que se admiten, pero a menos que mantenga una aplicación para una versión muy antigua de Windows, debe instalar la versión más reciente del SDK de Windows. Puede descargar la versión más reciente Windows SDK [aquí.](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

El SDK Windows admite el desarrollo de aplicaciones de 32 y 64 bits. Las WINDOWS están diseñadas para que el mismo código se pueda compilar para 32 o 64 bits sin cambios.

> [!Note]  
> El SDK Windows no admite el desarrollo de controladores de hardware y esta serie no trata el desarrollo de controladores. Para obtener información sobre cómo escribir un controlador de hardware, [vea Tareas iniciales con Windows controladores](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Siguientes

[Windows Convenciones de codificación](windows-coding-conventions.md)

## <a name="related-topics"></a>Temas relacionados

* [Descarga de Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Descargar Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)