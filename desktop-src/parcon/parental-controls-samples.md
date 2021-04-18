---
description: Ejemplos de controles parentales
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Ejemplos de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697519"
---
# <a name="parental-controls-samples"></a>Ejemplos de controles parentales

El código de ejemplo para controles parentales está disponible en ruta de acceso <installation directory> \\ ejemplos de Windows \\ <version number> \\ \\ seguridad \\ ParentalControls. Los ejemplos son los siguientes:

## <a name="utilities"></a>Sectores públicos

Funcionalidad auxiliar para la administración básica de COM, las operaciones de cadenas de SID y la funcionalidad de lectura y escritura de WMI. Todos los demás ejemplos dependen de este proyecto, a menos que se especifique lo contrario.

## <a name="complianceapi"></a>ComplianceAPI

Aplicación de consola controlada por línea de comandos que muestra cómo usar la API de cumplimiento para recuperar un subconjunto clave de la configuración de un usuario.

## <a name="complianceapp"></a>ComplianceApp

Aplicación de consola simple que muestra el uso de la API de cumplimiento para comprobar el registro necesario y las restricciones específicas. Si se habilitan las restricciones de tiempo, la aplicación también espera los eventos de cierre de sesión inminentes.

## <a name="uiextensibility"></a>UIExtensibility

Aplicación de consola controlada por línea de comandos en la que se muestra el uso de las API de WMI y el esquema WPC para enumerar, consultar, agregar, modificar y eliminar entradas de vínculo de extensibilidad de la interfaz de usuario.

Ejemplo de línea de comandos para el ejemplo:

"D: \\ WPC \\ Samples \\ Security \\ ParentalControls \\ UIExtensibility \\ Debug \\ UIExtensibility" Add/g: {FD59BB7F-54AB-11DB-9666-00E08161165F}/c: 0/N: D:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-101/S: d:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-103/I: d:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-104/D: d:/WPC/samples/Security/ParentalControls/UiExtRC/Debug/UiExtRC.dll,-106/e: c: \\ Windows \\Notepad.exe

donde UiExtRC es un archivo DLL de recursos simple con recursos de cadena para los IDENTIFICADOres 101 y 103, y 24x24 pixel 32-bit con mapas de bits alfa para los recursos 104 y 106.

## <a name="webextensibility"></a>WebExtensibility

Aplicación de consola controlada por línea de comandos que muestra cómo usar las API de WMI y el esquema WPC para enumerar, agregar y eliminar entradas de aplicación HTTP o de exención de URL, y para establecer y restablecer una invalidación de filtro de contenido web con las propiedades FilterID y FilterName.

No se muestra el acceso a la aplicación HTTP de solo lectura y a las listas de exenciones de URL, pero el código para leer las listas sería el mismo que para el caso de lectura/escritura, excepto para la modificación del parámetro WMI.

 

 



