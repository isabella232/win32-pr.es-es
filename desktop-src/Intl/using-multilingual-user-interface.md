---
description: Uso de Interfaz de usuario multilingüe
ms.assetid: caf167ad-f9a8-4093-9581-57bc507d1f6a
title: Uso de Interfaz de usuario multilingüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287acc88d144c7775d2125cbb4a055784370d87f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254835"
---
# <a name="using-multilingual-user-interface"></a>Uso de Interfaz de usuario multilingüe

En esta sección se describe cómo usar la funcionalidad Interfaz de usuario multilingüe (MUI) para diseñar e implementar las aplicaciones. A continuación se incluyen aspectos de la tecnología DEA que entrarán en juego en la mayoría de las fases del ciclo de vida de la aplicación.

-   Desarrollo de aplicaciones, incluida la preparación de recursos, la configuración de las preferencias del idioma de la aplicación, la búsqueda y carga de recursos
-   Creación y localización de la aplicación
-   Implementación de la aplicación

Estas son algunas preguntas que se deben tener en cuenta al diseñar e implementar una aplicación DE INTERFAZ DE USUARIO.

-   ¿Cuáles son las versiones de Windows que admitirá la aplicación?
-   ¿En qué idiomas se traducirá la aplicación?
-   ¿La configuración del idioma de la aplicación debe seguir siempre la configuración de idioma del sistema operativo o el usuario de la aplicación debe poder establecer idiomas específicos?
-   ¿Qué tipo de recursos de interfaz de usuario usa la aplicación y dónde se almacenan?

Esta sección incluye los temas siguientes. En las descripciones se da por supuesto que se ha destinado a Windows Vista y versiones posteriores. Los recursos de esta aplicación son recursos win32, con recursos específicos del lenguaje y código ejecutable que reside en archivos Win32 PE independientes. Se agregan consideraciones especiales para la compatibilidad con sistemas operativos Windows Vista o para distintos tipos de recursos según corresponda.

-   [Preparación de recursos](preparing-resources.md)
-   [Establecer las preferencias de idioma de la aplicación](setting-application-language-preferences.md)
-   [Búsqueda de recursos de Win32 PE](locating-win32-pe-resources.md)
-   [Buscar recursos de PE que no son win32](locating-non-win32-pe-resources.md)
-   [Localización de recursos y creación de la aplicación](localizing-resources-and-building-the-application.md)
-   [MUI: Ejemplo de aplicación Configuración sistema](mui-system-settings-application-sample.md)
-   [MUI: Application-Specific Configuración ejemplo (Windows Vista)](mui-application-specific-settings-sample-vista.md)
-   [MUI: Application-Specific Configuración de datos (Windows Vista)](mui-application-specific-settings-sample-pre-vista.md)

 

 



