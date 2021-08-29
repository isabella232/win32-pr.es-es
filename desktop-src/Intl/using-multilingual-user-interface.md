---
description: Uso de Interfaz de usuario multilingüe
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Uso de Interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00bcd970b71957fe865f30d031d0706f37cccdbd527ee65fb6e4a812f2836bb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764625"
---
# <a name="using-multilingual-user-interface"></a>Uso de Interfaz de usuario multilingüe

En esta sección se describe cómo usar la funcionalidad Interfaz de usuario multilingüe (para diseñar e implementar las aplicaciones. A continuación se incluyen aspectos de la tecnología DEA que entrarán en juego en la mayoría de las fases del ciclo de vida de la aplicación.

-   Desarrollo de aplicaciones, incluida la preparación de recursos, la configuración de las preferencias del lenguaje de la aplicación, la búsqueda y carga de recursos
-   Creación y localización de la aplicación
-   Implementación de la aplicación

Estas son algunas preguntas que se deben tener en cuenta al diseñar e implementar una aplicación DE LAN.

-   ¿Cuáles son las versiones Windows que admitirá la aplicación?
-   ¿En qué idiomas se localizará la aplicación?
-   ¿Debe la configuración del idioma de la aplicación seguir siempre la configuración de idioma del sistema operativo o debe poder establecer idiomas específicos por parte del usuario de la aplicación?
-   ¿Qué tipo de recursos de interfaz de usuario usa la aplicación y dónde se almacenan?

Esta sección incluye los temas siguientes. En las descripciones se da por supuesto que una aplicación DE INTERFAZ de usuario está destinada a Windows Vista y versiones posteriores. Los recursos de esta aplicación son recursos de Win32, con recursos específicos del lenguaje y código ejecutable que reside en archivos Win32 PE independientes. Se agregan consideraciones especiales para la compatibilidad con sistemas operativos Windows Vista o para diferentes tipos de recursos según corresponda.

-   [Preparación de recursos](preparing-resources.md)
-   [Establecer las preferencias del idioma de la aplicación](setting-application-language-preferences.md)
-   [Búsqueda de recursos de Win32 PE](locating-win32-pe-resources.md)
-   [Buscar recursos de PE que no son win32](locating-non-win32-pe-resources.md)
-   [Localización de recursos y creación de la aplicación](localizing-resources-and-building-the-application.md)
-   [MUI: Ejemplo de aplicación Configuración sistema](mui-system-settings-application-sample.md)
-   [MUI: Application-Specific Configuración de ejemplo (Windows Vista)](mui-application-specific-settings-sample-vista.md)
-   [MUI: Application-Specific Configuración de ejemplo (Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)

 

 



