---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Cuadro de diálogo común de Win32 ChooseFont ()
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717132"
---
# <a name="choosefont-win32-common-dialog"></a>Cuadro de diálogo común de Win32 ChooseFont ()

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad** baja  
**Frecuencia** : medio  




## <a name="description"></a>Descripción

Windows 7 incluye varias actualizaciones en el cuadro de diálogo común de Win32 ChooseFont (). Estas se dividen en dos categorías:

-   Actualización visual del cuadro de diálogo
-   Compatibilidad con las nuevas características de mostrar u ocultar fuentes

La **actualización del cuadro de diálogo** actualiza la plantilla estándar para que el cuadro de diálogo se muestre más en línea con otros diseños de cuadro de diálogo de Windows. Presenta WYSIWYG a las listas de presentación de fuentes para ayudar a los usuarios a elegir fuentes. También incluye un vínculo al CPL Fonts para facilitar el acceso a los usuarios que deseen personalizar sus listas de fuentes.

**Mostrar u ocultar fuentes** es una nueva característica de la plataforma Windows 7 en la que las fuentes no adecuadas para la configuración de idioma del usuario actual (métodos de entrada) no se presentan de forma predeterminada en las listas de selección de fuentes. Los usuarios pueden personalizar las fuentes que deseen que aparezcan en el CPL de fuentes o deshabilitar esta característica.

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

**Actualización visual del cuadro de diálogo**

Hemos incorporado dos nuevas plantillas en Windows 7 (una para las aplicaciones que cargan la versión 6 o posterior de comctl32.dll y otra para las aplicaciones que cargan versiones anteriores).

-   Por motivos de compatibilidad de aplicaciones, estas nuevas plantillas solo se cargan para las aplicaciones que no enlazan la cola de mensajes ChooseFont. Las aplicaciones que enlazan la cola de mensajes seguirán viendo el diseño del cuadro de diálogo antiguo.
-   Las aplicaciones que proporcionan sus propias plantillas seguirán pudiendo usarlas.

Las aplicaciones que no obtienen las nuevas plantillas no verán cambios de diseño de cuadros de diálogo de vista. Sin embargo, todavía deben obtener la nueva versión preliminar de la fuente WYSIWYG.

**Mostrar u ocultar fuentes**

En todas las versiones de ChooseFont, el cuadro de diálogo usará la configuración de fuente Mostrar u ocultar del usuario actual para determinar la lista de fuentes que se va a mostrar. Esto hará que se muestren menos listas de fuentes en la mayoría de las instancias.

## <a name="end-user-mitigation"></a>Mitigación del usuario final

**Mostrar u ocultar fuentes:** Para deshabilitar la ocultación de fuentes, los usuarios deben ir a la página de configuración de fuentes del CPL de fuentes y anular la selección del

Casilla "ocultar fuentes según la configuración de idioma"

## <a name="developer-mitigation"></a>Mitigación del desarrollador

-   **Actualización visual:** Los desarrolladores de aplicaciones que proporcionan sus propias plantillas pueden querer actualizar esto para que esté en línea con la nueva plantilla de Windows 7 adecuada. Las nuevas plantillas están disponibles en el archivo de plantilla Font. Dlg.

    **Nota:** La nueva plantilla publicada contiene un control SysLink adicional que proporciona un acceso directo que permite a los usuarios iniciar el CPL Fonts para mostrar más fuentes. El control de vínculo requiere la versión 6 de la biblioteca de controles comunes de Windows (comctl32.dll). Los desarrolladores deben proporcionar un manifiesto o una directiva que especifique el uso de la versión 6 del archivo DLL si está disponible. En el caso de que una aplicación use una versión anterior de la biblioteca de controles comunes, use en su lugar el tipo de control "PUSHBUTTON".

-   **Mostrar u ocultar fuentes:** Los desarrolladores pueden deshabilitar esta característica proporcionando una marca adicional (CF \_ INACTIVEFONTS) en el miembro flags de la estructura CHOOSEFONT. Al establecer esta marca, se muestran todas las fuentes instaladas en la lista fuente.
-   **Mostrar u ocultar fuentes:** Las aplicaciones que proporcionan contenido de la ayuda de ChooseFont pueden querer agregar contenido para explicar por qué se reduce la lista de fuentes y dirigir a los usuarios al CPL de fuentes para personalizar sus listas de fuentes.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Los desarrolladores cuyas aplicaciones enlazan la cola de mensajes ChooseFont para personalizar el cuadro de diálogo deben comprobar que sus aplicaciones conservan toda la funcionalidad existente.

Las aplicaciones que recortan drásticamente la lista de fuentes mediante marcas deben asegurarse de que la lista de fuentes presentada siga siendo aceptable.

 

 



