---
description: Ejemplos de controles parentales
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: Ejemplos de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23111e42b670c30630b7ebd250c94ba2f148fcf4a81874fcc3c360db9b4bbd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971614"
---
# <a name="parental-controls-samples"></a>Ejemplos de controles parentales

El código de ejemplo para los controles parentales está disponible en la ruta <installation directory> \\ Windows ejemplos de \\ <version number> \\ \\ seguridad \\ ParentalControls. Los ejemplos son los siguientes:

## <a name="utilities"></a>Utilidades

Funcionalidad auxiliar para la administración COM básica, las operaciones de cadena de SID y la funcionalidad de lectura y escritura de WMI. Todos los demás ejemplos dependen de este proyecto, a menos que se especifique lo contrario.

## <a name="complianceapi"></a>ComplianceAPI

Aplicación de consola controlada por la línea de comandos que muestra cómo usar compliance API para recuperar un subconjunto clave de configuración para un usuario.

## <a name="complianceapp"></a>ComplianceApp

Aplicación de consola sencilla que muestra el uso de la API de cumplimiento para comprobar si hay restricciones específicas y necesarias para el registro. Si se habilitan las restricciones de tiempo, la aplicación también espera los eventos de cierre de sesión que se van a cerrar.

## <a name="uiextensibility"></a>UIExtensibility

Aplicación de consola controlada por la línea de comandos que muestra el uso de las API WMI y el esquema de WPC para enumerar, consultar, agregar, modificar y eliminar entradas de vínculo de extensibilidad de la interfaz de usuario.

Línea de comandos de ejemplo para el ejemplo:

"D: \\ WPC \\ Samples Security \\ \\ ParentalControls \\ UIExtensibility \\ debug \\ UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c: \\ windows \\Notepad.exe

donde UiExtRC es un archivo DLL de recursos simple con recursos de cadena para los identificadores 101 y 103, y 24 x 24 píxeles de 32 bits con mapas de bits alfa para los recursos 104 y 106.

## <a name="webextensibility"></a>WebExtensibility

Aplicación de consola controlada por la línea de comandos que muestra cómo usar las API wmi y el esquema de WPC para enumerar, agregar y eliminar entradas de exención de url o aplicación HTTP, y para establecer y restablecer una invalidación del filtro de contenido web con las propiedades FilterID y FilterName.

No se muestra el acceso a la aplicación HTTP de solo lectura y a las listas de exención de dirección URL, pero el código para leer las listas sería el mismo que para el caso de lectura y escritura, excepto para la modificación del parámetro WMI.

 

 



