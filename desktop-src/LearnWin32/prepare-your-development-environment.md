---
title: Preparación del entorno de desarrollo
description: Preparación del entorno de desarrollo
ms.assetid: 5a3fd27e-ec8f-41eb-9d31-86d6d9f70862
ms.topic: article
ms.date: 10/03/2019
ms.openlocfilehash: ec42509ea81efce4bb17365d3bf08d36c2a4f415
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358906"
---
# <a name="prepare-your-development-environment"></a>Preparación del entorno de desarrollo

Para escribir un programa de Windows en C o C++, debe instalar el kit de desarrollo de software (SDK) de Microsoft Windows o Microsoft Visual Studio. El Windows SDK contiene los encabezados y las bibliotecas necesarios para compilar y vincular la aplicación. El Windows SDK también contiene herramientas de línea de comandos para compilar aplicaciones de Windows, incluidas la Visual C++ compilador y el vinculador. Aunque puede compilar y compilar programas de Windows con las herramientas de línea de comandos, se recomienda usar Microsoft Visual Studio. Puede descargar una descarga gratuita de Visual Studio Community o pruebas gratuitas de otras versiones de Visual Studio [aquí](https://visualstudio.microsoft.com/downloads/).

Cada versión de la Windows SDK tiene como destino la versión más reciente de Windows, así como varias versiones anteriores. En las notas de la versión se enumeran las plataformas específicas que se admiten, pero a menos que esté manteniendo una aplicación para una versión anterior de Windows, debe instalar la versión más reciente de la Windows SDK. Puede descargar la Windows SDK más reciente [aquí](https://developer.microsoft.com/windows/downloads/windows-10-sdk).

El Windows SDK admite el desarrollo de aplicaciones de 32 bits y de 64 bits. Las API de Windows están diseñadas para que el mismo código se pueda compilar para 32 bits o 64 bits sin cambios.

> [!Note]  
> El Windows SDK no admite el desarrollo de controladores de hardware, y esta serie no tratará el desarrollo de controladores. Para obtener información acerca de cómo escribir un controlador de hardware, consulte [Introducción con controladores de Windows](/windows-hardware/drivers/gettingstarted/).

## <a name="next"></a>Siguientes

[Convenciones de codificación de Windows](windows-coding-conventions.md)

## <a name="related-topics"></a>Temas relacionados

* [Descarga de Visual Studio](https://visualstudio.microsoft.com/downloads/)
* [Descargar Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)