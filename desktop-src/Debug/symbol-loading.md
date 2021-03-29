---
description: El controlador de símbolos cargará los símbolos cuando se llame a la función SymInitialize con el parámetro fInvadeProcess establecido en TRUE o cuando se llame a la función SymLoadModuleEx para especificar un módulo.
ms.assetid: fae1895e-9fed-45e3-8ecf-4c6cc67a6094
title: Carga de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705a7af3525c784b2bbcd512b267309a466a11c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423223"
---
# <a name="symbol-loading"></a>Carga de símbolos

El controlador de símbolos cargará los símbolos cuando se llame a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) con el parámetro *FInvadeProcess* establecido en **true** o cuando se llame a la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) para especificar un módulo. En cualquier caso, el controlador de símbolos carga los símbolos o pospone la carga de símbolos hasta que se solicitan símbolos, dependiendo de las opciones establecidas por la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) .

El controlador de símbolos se puede usar para recuperar información simbólica de cualquier módulo; no es necesario asociarlo a un proceso especificado en la llamada a [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Para usar un módulo arbitrario, especifique la ruta de acceso completa a la imagen del módulo en el parámetro *ImageName* . Puede usar una ruta de acceso a cualquier módulo ejecutable que tenga información de depuración (. exe,. dll,. drv,. sys,. SCR,. cpl o. com). Use el parámetro *BaseOfDll* para especificar cualquier dirección de carga y, a continuación, las direcciones de símbolos se basarán en esa dirección.

Puede que no sea necesario mantener un módulo de símbolos cargado a lo largo de la duración de una aplicación. Para liberar el módulo de símbolos de la lista de módulos del controlador de símbolos, utilice la función [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule) . Esta función libera la memoria asignada para el módulo Symbol. Para utilizar símbolos para ese módulo de nuevo, debe llamar a la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) incluso si se establece la opción de carga diferido de símbolos.

## <a name="diagnosing-symbol-load-problems"></a>Diagnóstico de problemas de carga de símbolos

Para ver todos los intentos de carga de símbolos, llame a [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) con SYMOPT \_ Debug. Esto hace que DbgHelp llame a la función [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) con información detallada sobre las búsquedas de símbolos, como los directorios en los que está buscando y los mensajes de error. Si el código usa [**SymRegisterCallback64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symregistercallback), DbgHelp llamará a la función de devolución de llamada en lugar de llamar a **OutputDebugString**. El parámetro *ActionCode* se establece en CBA \_ Debug \_ info y el parámetro *CallbackData* es una cadena que se puede mostrar.

Para habilitar esta salida de depuración para que se muestre en la consola sin cambiar el código fuente, establezca la \_ variable de entorno DBGHELP DBGOUT en un valor distinto de **null** antes de llamar a la función [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Para registrar la información en un archivo, establezca la \_ variable de entorno del registro DBGHELP en el nombre del archivo de registro que se va a usar.

Tenga en cuenta que estas características solo deben usarse cuando sea necesario. Pueden ralentizar la carga de símbolos de módulos que contienen muchos símbolos.

 

 
