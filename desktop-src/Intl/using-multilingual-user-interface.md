---
description: Uso de la interfaz de usuario multilingüe
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Uso de la interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279494"
---
# <a name="using-multilingual-user-interface"></a>Uso de la interfaz de usuario multilingüe

En esta sección se describe cómo usar la funcionalidad de la interfaz de usuario multilingüe (MUI) para diseñar e implementar aplicaciones. A continuación se muestran aspectos de la tecnología de MUI que entrarán en juego en la mayoría de las fases del ciclo de vida de la aplicación.

-   Desarrollo de aplicaciones, incluida la preparación de recursos, la configuración de las preferencias de idioma de la aplicación, la búsqueda y carga de recursos
-   Compilar y localizar la aplicación
-   Implementación de la aplicación

Estas son algunas preguntas a tener en cuenta al diseñar e implementar una aplicación de MUI.

-   ¿Cuáles son las versiones de Windows compatibles con la aplicación?
-   ¿En qué idiomas se localizará la aplicación?
-   ¿La configuración de idioma de la aplicación siempre sigue la configuración de idioma para el sistema operativo o si el usuario de la aplicación puede establecer idiomas específicos?
-   ¿Qué tipo de recursos de interfaz de usuario usa la aplicación y dónde se almacenan?

Esta sección incluye los temas siguientes. Las descripciones suponen una aplicación de MUI destinada a Windows Vista y versiones posteriores. Los recursos de esta aplicación son recursos de Win32, con recursos específicos del lenguaje y código ejecutable que residen en archivos PE de Win32 independientes. Las consideraciones especiales para la compatibilidad con los sistemas operativos anteriores a Windows Vista o para distintos tipos de recursos se agregan según corresponda.

-   [Preparación de recursos](preparing-resources.md)
-   [Configuración de las preferencias de idioma de la aplicación](setting-application-language-preferences.md)
-   [Ubicar recursos PE de Win32](locating-win32-pe-resources.md)
-   [Ubicar recursos de PE que no son de Win32](locating-non-win32-pe-resources.md)
-   [Localizar recursos y compilar la aplicación](localizing-resources-and-building-the-application.md)
-   [MUI: ejemplo de la aplicación de configuración del sistema](mui-system-settings-application-sample.md)
-   [MUI: ejemplo de configuración de Application-Specific (Windows Vista)](mui-application-specific-settings-sample-vista.md)
-   [MUI: ejemplo de configuración de Application-Specific (anterior a Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)

 

 



