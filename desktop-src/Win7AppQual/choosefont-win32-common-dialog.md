---
description: Cuadro de diálogo común chooseFont() Win32
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Cuadro de diálogo común chooseFont() Win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4dd8eb6ec226f8dbf5220f5a90dac802cf149dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571028"
---
# <a name="choosefont-win32-common-dialog"></a>Cuadro de diálogo común chooseFont() Win32

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** baja  
**Frecuencia:** media  




## <a name="description"></a>Descripción

Windows 7 incluye varias actualizaciones del cuadro de diálogo común ChooseFont() Win32. Se divide en dos categorías:

-   Actualización visual del cuadro de diálogo
-   Compatibilidad con la nueva característica mostrar u ocultar fuentes

La **actualización del cuadro de** diálogo actualiza la plantilla estándar para que el diálogo se alinee más con otros diseños de diálogo de Windows. Se presenta WYSIWYG en las listas de visualización de fuentes para ayudar a los usuarios a elegir fuentes. También incluye un vínculo a la CPL Fuentes para proporcionar un acceso sencillo a los usuarios que desean personalizar sus listas de fuentes.

**Mostrar u** ocultar fuentes es una nueva característica de la plataforma Windows 7 en la que las fuentes no adecuadas para la configuración de idioma del usuario actual (métodos de entrada) no se presentan de forma predeterminada en las listas de selección de fuentes. Los usuarios pueden personalizar las fuentes que desean que aparezcan en la CPL fuentes o pueden deshabilitar esta característica.

## <a name="manifestation-of-impact"></a>Demostración de impacto

**Actualización del objeto visual de cuadro de diálogo**

Hemos introducido dos nuevas plantillas en Windows 7 (una para las aplicaciones que cargan la versión 6 o posterior de comctl32.dll y otra para las aplicaciones que cargan versiones anteriores).

-   Por motivos de compatibilidad de aplicaciones, estas nuevas plantillas solo se cargarán para las aplicaciones que no enlacen la cola de mensajes ChooseFont. Las aplicaciones que enlacen la cola de mensajes seguirán ven el diseño del cuadro de diálogo anterior.
-   Las aplicaciones que proporcionan sus propias plantillas seguirán siendo capaces de usarlas.

Las aplicaciones que no obtienen las nuevas plantillas no verán ningún cambio en el diseño del cuadro de diálogo de Vista. Sin embargo, todavía deben obtener la nueva versión preliminar de fuente DEWYG DE WYSIWYG.

**Mostrar u ocultar fuentes**

Para todas las versiones de ChooseFont, el cuadro de diálogo usará la configuración de fuente mostrar u ocultar del usuario actual para determinar la lista de fuentes que se va a mostrar. Esto dará como resultado la presentación de menos listas de fuentes en la mayoría de las instancias.

## <a name="end-user-mitigation"></a>Mitigación del usuario final

**Mostrar u ocultar fuentes:** Para deshabilitar la ocultación de fuentes, los usuarios deben ir a la página Font Configuración del CPL Fonts y anular la selección de '

Casilla "Ocultar fuentes según la configuración de idioma"

## <a name="developer-mitigation"></a>Mitigación para desarrolladores

-   **Actualización visual:** Es posible que los desarrolladores de aplicaciones que proporcionan sus propias plantillas deban actualizarla para que se alineen con la nueva plantilla Windows 7. Las nuevas plantillas están disponibles en el archivo de plantilla Font.dlg.

    **Nota:** La nueva plantilla publicada contiene un control SysLink adicional que proporciona un acceso directo que permite a los usuarios iniciar la CPL fuentes para mostrar más fuentes. El control de vínculo requiere la versión 6 de la Windows de control común (comctl32.dll). Los desarrolladores deben proporcionar un manifiesto o una directiva que especifique el uso de la versión 6 del archivo DLL si está disponible. Cuando una aplicación use una versión anterior de la biblioteca de controles común, use el tipo de control "PUSHBUTTON" en su lugar.

-   **Mostrar u ocultar fuentes:** Los desarrolladores pueden deshabilitar esta característica proporcionando una marca adicional (CF \_ INACTIVEFONTS) en el miembro flags de la estructura CHOOSEFONT. Al establecer esta marca, todas las fuentes instaladas se muestran en la lista de fuentes.
-   **Mostrar u ocultar fuentes:** Las aplicaciones que proporcionan contenido de ayuda de ChooseFont pueden desear agregar contenido para explicar por qué se reduce la lista de fuentes y dirigir a los usuarios a la CPL fuentes para personalizar sus listas de fuentes.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Los desarrolladores cuyas aplicaciones enlacen la cola de mensajes ChooseFont para personalizar el cuadro de diálogo deben comprobar que sus aplicaciones conservan toda la funcionalidad existente.

Las aplicaciones que recortan en gran medida la lista de fuentes mediante marcas deben asegurarse de que la lista de fuentes presentada sigue siendo aceptable.

 

 



