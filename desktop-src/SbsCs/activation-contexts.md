---
description: Los contextos de activación son estructuras de datos en memoria que contienen información que el sistema puede usar para redirigir una aplicación para cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Contextos de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1f20d747f63ba71eee73fc17c0d5543003e5f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271775"
---
# <a name="activation-contexts"></a>Contextos de activación

[*Los contextos de activación*](a-sbscs-gly.md) son estructuras de datos en memoria que contienen información que el sistema puede usar para redirigir una aplicación para cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada. Una sección del contexto de activación puede contener información de redireccionamiento de DLL que usa el cargador de DLL; Otra sección puede contener información del servidor COM. Las funciones de contexto de activación usan, crean, activan y desactivan contextos de activación. Las funciones de activación pueden redirigir el enlace de una aplicación a objetos con nombre de versión que especifican determinadas versiones de DLL, clases de ventana, servidores COM, bibliotecas de tipos e interfaces. Para obtener más información sobre las funciones y estructuras del contexto de activación, vea La referencia de [contexto de activación](activation-context-reference.md).

A partir Windows XP, las funciones de contexto de activación Windows usar información en [manifiestos](manifests.md) para crear objetos con nombre de versión. Si una aplicación crea un proceso mediante una llamada a [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa), Windows comprueba la existencia de un manifiesto [de aplicación](application-manifests.md). Si existe un manifiesto, Windows la información del manifiesto para rellenar el contexto de activación. Dado que los manifiestos describen la dependencia de una aplicación en las versiones de ensamblado en paralelo, los objetos especificados sin versiones en el manifiesto se asignan a objetos con nombre de versión. [](about-side-by-side-assemblies-.md) Por ejemplo, el manifiesto puede describir archivos DLL, archivos, clases de ventana, servidores COM, bibliotecas de tipos e interfaces.

Cuando se crea un objeto global dentro del contexto de activación, el sistema asigna automáticamente al objeto un nombre específico de la versión consultando el manifiesto. Cuando la aplicación se ejecuta y solicita un objeto con nombre, obtiene el objeto con nombre de versión. Esto permite que varias versiones de un módulo de código se ejecuten en el sistema al mismo tiempo sin interferir entre sí. Por ejemplo, [Windows Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) usa un manifiesto para describir una dependencia de la versión 6.0 de COMCTL32 y para crear versiones de clases de ventana.

Si una aplicación crea un recurso mediante una llamada a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), el proceso especifica un nombre de clase para esa función. La llamada a [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) obtiene el contexto de activación actual y comprueba si existe una asignación para el nombre de clase especificado. Si existe una asignación, usará esa versión del proceso de llamada para resolver la asignación y proporcionar el nombre de clase específico de la versión. Windows crea una ventana con el procedimiento de ventana, los estilos y otros atributos asociados a ese nombre y versión de clase.

El sistema administra el contexto de activación en la mayoría de los casos. Los desarrolladores de aplicaciones y los proveedores de ensamblados no necesitan normalmente realizar llamadas a la pila. Las aplicaciones pueden administrar un contexto de activación llamando directamente al contexto de activación. Para más información, consulte [Uso de activation Context API.](using-the-activation-context-api.md)

 

 
