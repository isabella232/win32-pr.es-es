---
description: Los contextos de activación son estructuras de datos en memoria que contienen información que el sistema puede utilizar para redirigir una aplicación para cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Contextos de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1f20d747f63ba71eee73fc17c0d5543003e5f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360665"
---
# <a name="activation-contexts"></a>Contextos de activación

Los [*contextos de activación*](a-sbscs-gly.md) son estructuras de datos en memoria que contienen información que el sistema puede utilizar para redirigir una aplicación para cargar una versión de dll determinada, una instancia de objeto com o una versión de ventana personalizada. Una sección del contexto de activación puede contener información de redirección de DLL que usa el cargador de DLL. otra sección puede contener información del servidor COM. Las funciones de contexto de activación usan, crean, activan y desactivan contextos de activación. Las funciones de activación pueden redirigir el enlace de una aplicación a objetos con nombre de versión que especifican versiones de archivos DLL, clases de ventanas, servidores COM, bibliotecas de tipos e interfaces determinadas. Para obtener más información sobre las funciones y estructuras de contexto de activación, vea la [referencia de contexto de activación](activation-context-reference.md).

A partir de Windows XP, las funciones de contexto de activación permiten a Windows usar información en los [manifiestos](manifests.md) para crear objetos con nombre de versión. Si una aplicación crea un proceso llamando a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), Windows comprueba la existencia de un [manifiesto de aplicación](application-manifests.md). Si existe un manifiesto, Windows usa la información del manifiesto para rellenar el contexto de activación. Dado que los manifiestos describen la dependencia de una aplicación en las versiones de [ensamblado en paralelo](about-side-by-side-assemblies-.md) , los objetos especificados sin versiones en el manifiesto se asignan a objetos con nombre de versión. Por ejemplo, el manifiesto puede describir dll, archivos, clases de ventana, servidores COM, bibliotecas de tipos e interfaces.

Cuando se crea un objeto global en el contexto de activación, el sistema asigna automáticamente al objeto un nombre específico de la versión mediante la consulta del manifiesto. Cuando la aplicación ejecuta y solicita un objeto con nombre, obtiene el objeto con nombre de versión. Esto permite que varias versiones de un módulo de código se ejecuten en el sistema al mismo tiempo sin interferir entre sí. Por ejemplo, el [Shell de Windows](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) usa un manifiesto para describir una dependencia de la versión 6,0 de comctl32 y para crear versiones de las clases de ventana.

Si una aplicación crea un recurso mediante una llamada a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), el proceso especifica un nombre de clase para esa función. La llamada a [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) obtiene el contexto de activación actual y comprueba si existe una asignación para el nombre de clase especificado. Si existe una asignación, usará esa versión del proceso de llamada para resolver la asignación y proporcionar el nombre de clase específico de la versión. Windows crea una ventana con el procedimiento de ventana, los estilos y otros atributos asociados a ese nombre de clase y versión.

El sistema administra el contexto de activación en la mayoría de los casos. Normalmente, los desarrolladores de aplicaciones y los proveedores de ensamblados no necesitan realizar llamadas a la pila. Las aplicaciones pueden administrar un contexto de activación llamando directamente al contexto de activación. Para obtener más información, consulte [uso de la API de contexto de activación](using-the-activation-context-api.md).

 

 
