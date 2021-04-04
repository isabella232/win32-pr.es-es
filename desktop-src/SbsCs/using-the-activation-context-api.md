---
description: Las aplicaciones pueden administrar un contexto de activación llamando directamente a las funciones de contexto de activación.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Uso de la API de contexto de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154092"
---
# <a name="using-the-activation-context-api"></a>Uso de la API de contexto de activación

Las aplicaciones pueden administrar un [contexto de activación](activation-contexts.md) llamando directamente a las funciones de contexto de activación. Los contextos de activación son estructuras de datos en memoria. El sistema puede utilizar la información del contexto de activación para redirigir una aplicación para cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada. Para obtener más información, vea [referencia de contexto de activación](activation-context-reference.md).

La interfaz de programación de aplicaciones (API) se puede usar para administrar el contexto de activación y crear objetos con nombre de versión con [manifiestos](manifests.md). Los dos escenarios siguientes muestran cómo una aplicación puede administrar un contexto de activación llamando directamente a las funciones de contexto de activación. Sin embargo, en la mayoría de los casos, el sistema administra el contexto de activación. Normalmente, los desarrolladores de aplicaciones y los proveedores de ensamblados no necesitan realizar llamadas a la pila para administrar el contexto de activación.

-   Procesos y aplicaciones que implementan capas de distribución o direccionamiento indirecto.

    Por ejemplo, un usuario que administra contextos de activación en el bucle de eventos. Cada vez que se tiene acceso a la ventana, por ejemplo moviendo el mouse sobre la ventana, se llama a [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) , que activa el contexto de activación actual para el recurso, tal como se muestra en el siguiente fragmento de código.

    <dl> CONTROLAR hActCtx;  
    CreateWindow ();  
    ...  
    GetCurrentActCtx (&ActCtx);  
    ...  
    ReleaseActCtx (&ActCtx);  
    </dl>

    En el fragmento de código siguiente, la función de la API activa los contextos de activación adecuados antes de llamar a [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca). Cuando se llama a **CallWindowProc** , usa este contexto para pasar un mensaje a Windows. Cuando se hayan completado todas las operaciones de recursos, la función desactivará el contexto.

    <dl> ULONG \_ ptr ulpCookie;  
    CONTROLAR hActCtx;  
    Si (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    CallWindowProc(...);  
    ...  
    DeactivateActCtx (0, ulpCookie);  
    }  
    </dl>

-   Capa de distribución del delegado.

    Este escenario se aplica a los administradores que administran varias entidades con un nivel de API común, como un administrador de controladores. Aunque aún no se ha implementado, un ejemplo de esto sería el controlador ODBC.

    En este escenario, el nivel intermedio es capaz de procesar enlaces de ensamblado. Para obtener el controlador de enlace específico de la versión, los publicadores deben proporcionar un manifiesto y especificar dependencias en componentes específicos de ese manifiesto. La aplicación base no se enlaza de forma dinámica a los componentes; en tiempo de ejecución, el administrador de controladores administra las llamadas. Cuando se llama al controlador ODBC en función de la cadena de conexión, se carga el controlador adecuado. Después crea el contexto de activación con la información del archivo de manifiesto del ensamblado.

    Sin el manifiesto, la acción predeterminada para el controlador es usar el mismo contexto que el especificado por la aplicación, en este ejemplo, la versión 2 de MSVCRT. Como existe un manifiesto, se establece un contexto de activación independiente. Cuando se ejecuta el controlador ODBC, se enlaza a la versión 1 del ensamblado MSVCRT.

    Cada vez que el administrador de controladores llama a la capa de envío (por ejemplo, para obtener el siguiente conjunto de datos), usa los ensamblados adecuados basados en el contexto de activación. En el fragmento de código siguiente se muestra esto.

    <dl> CONTROLAR hActCtx;  
    ULONG \_ ptr ulpCookie;  
    ACTCTX ActCtxToCreate = {...};  
    hActCtx = CreateActCtx (&ActCtxToCreate);  
    ...;  
    Si (ActivateActCtx (hActCtx, &ulpCookie))  
    {  
    ...  
    ConnectDb(...);  
    DeactivateActCtx (0, ulpCookie);  
    }  
    ...  
    ReleaseActCtx(hActCtx);  
    </dl>

 

 
