---
description: Una biblioteca Dynamic-Link (DLL) puede contener datos globales o datos locales.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Dynamic-Link library data
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8902eb6388624d958c7176a14b8893f8e2245ddd9370f6ba2ac71605b2379cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048445"
---
# <a name="dynamic-link-library-data"></a>Dynamic-Link library data

Una biblioteca Dynamic-Link (DLL) puede contener datos globales o datos locales.

## <a name="variable-scope"></a>Ámbito de variable

El compilador y el vinculador tratan las variables que se declaran como globales en un archivo de código fuente DLL, pero cada proceso que carga un archivo DLL determinado obtiene su propia copia de las variables globales de ese archivo DLL. El ámbito de las variables estáticas se limita al bloque en el que se declaran las variables estáticas. Como resultado, cada proceso tiene su propia instancia de las variables globales y estáticas del archivo DLL de forma predeterminada.

> [!Note]  
> Las herramientas de desarrollo pueden permitirle invalidar el comportamiento predeterminado. Por ejemplo, el compilador Visual C++ admite **\# la sección pragma** y el vinculador admite la opción /SECTION. Para obtener más información, consulte la documentación incluida con las herramientas de desarrollo.

 

## <a name="dynamic-memory-allocation"></a>Memoria dinámica asignación

Cuando un archivo DLL asigna memoria mediante cualquiera de las funciones de asignación de memoria [**(GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)y [**VirtualAlloc),**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)la memoria se asigna en el espacio de direcciones virtuales del proceso de llamada y solo es accesible para los subprocesos de ese proceso.

Un archivo DLL puede usar la asignación de archivos para asignar memoria que se pueda compartir entre los procesos. Para obtener una explicación general sobre cómo usar la asignación de archivos para crear memoria compartida con nombre, vea [Asignación de archivos](/windows/desktop/Memory/file-mapping). Para obtener un ejemplo en el que se usa la función [**DllMain**](dllmain.md) para configurar la memoria compartida mediante la asignación de archivos, vea [Using Shared Memory in a Dynamic-Link Library](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>Almacenamiento local para el subproceso

Las funciones de almacenamiento local de subprocesos (TLS) permiten a un archivo DLL asignar un índice para almacenar y recuperar un valor diferente para cada subproceso de un proceso multiproceso. Por ejemplo, una aplicación de hoja de cálculo puede crear una nueva instancia del mismo subproceso cada vez que el usuario abre una nueva hoja de cálculo. Un archivo DLL que proporciona las funciones para varias operaciones de hoja de cálculo puede usar TLS para guardar información sobre el estado actual de cada hoja de cálculo (fila, columna, entre otras). Para obtener una explicación general del almacenamiento local de subprocesos, vea [Thread Local Storage](/windows/desktop/ProcThread/thread-local-storage). Para obtener un ejemplo que usa la función [**DllMain**](dllmain.md) para configurar el almacenamiento local de subprocesos, vea [Using Thread Local Storage in a Dynamic-Link Library](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 y Windows XP:** El Visual C++ admite una sintaxis que le permite declarar variables locales de subproceso: **\_ declspec(thread).** Si usa esta sintaxis en un archivo DLL, no podrá cargar el archivo DLL explícitamente mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) en versiones de Windows antes de Windows Vista. Si el archivo DLL se cargará explícitamente, debe usar las funciones de almacenamiento local del subproceso en lugar **\_ de declspec(thread).**

 

 
