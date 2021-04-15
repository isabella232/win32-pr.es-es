---
description: Una biblioteca de Dynamic-Link (DLL) puede contener datos globales o datos locales.
ms.assetid: b1f6811e-c413-4124-9ccb-ea59b7a8a7ff
title: Datos de la biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83280d3bfc449061c44f9e8bfd9b47833e7eca19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669705"
---
# <a name="dynamic-link-library-data"></a>Datos de la biblioteca Dynamic-Link

Una biblioteca de Dynamic-Link (DLL) puede contener datos globales o datos locales.

## <a name="variable-scope"></a>Ámbito de variable

Las variables que se declaran como globales en un archivo de código fuente DLL se tratan como variables globales por parte del compilador y del enlazador, pero cada proceso que carga un archivo DLL determinado obtiene su propia copia de las variables globales de ese archivo DLL. El ámbito de las variables estáticas se limita al bloque en el que se declaran las variables estáticas. Como resultado, cada proceso tiene su propia instancia de las variables globales y estáticas de DLL de forma predeterminada.

> [!Note]  
> Las herramientas de desarrollo pueden permitirle invalidar el comportamiento predeterminado. Por ejemplo, el compilador Visual C++ admite la **\# sección pragma** y el vinculador admite la opción/Section. Para obtener más información, consulte la documentación que se incluye con las herramientas de desarrollo.

 

## <a name="dynamic-memory-allocation"></a>Asignación Memoria dinámica

Cuando un archivo DLL asigna memoria mediante cualquiera de las funciones de asignación de memoria ([**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc), [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc)y [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc)), la memoria se asigna en el espacio de direcciones virtuales del proceso de llamada y solo es accesible para los subprocesos de ese proceso.

Un archivo DLL puede utilizar la asignación de archivos para asignar memoria que se puede compartir entre los procesos. Para obtener una explicación general sobre cómo usar la asignación de archivos para crear memoria compartida con nombre, consulte [asignación de archivos](/windows/desktop/Memory/file-mapping). Para obtener un ejemplo en el que se usa la función [**DllMain**](dllmain.md) para configurar la memoria compartida mediante la asignación de archivos, vea [uso de memoria compartida en una biblioteca de Dynamic-Link](using-shared-memory-in-a-dynamic-link-library.md).

## <a name="thread-local-storage"></a>Almacenamiento local para el subproceso

Las funciones de almacenamiento local de subprocesos (TLS) permiten a un archivo DLL asignar un índice para almacenar y recuperar un valor diferente para cada subproceso de un proceso multiproceso. Por ejemplo, una aplicación de hoja de cálculo puede crear una nueva instancia del mismo subproceso cada vez que el usuario abra una nueva hoja de cálculo. Un archivo DLL que proporciona las funciones para varias operaciones de hoja de cálculo puede utilizar TLS para guardar información sobre el estado actual de cada hoja de cálculo (fila, columna, etc.). Para obtener una explicación general del almacenamiento local de subprocesos, vea [almacenamiento local para el subproceso](/windows/desktop/ProcThread/thread-local-storage). Para obtener un ejemplo en el que se usa la función [**DllMain**](dllmain.md) para configurar el almacenamiento local de subprocesos, vea [usar el almacenamiento local para el subproceso en una biblioteca Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

**Windows Server 2003 y Windows XP:** El compilador Visual C++ admite una sintaxis que permite declarar variables locales de subproceso: **\_ declspec (Thread)**. Si utiliza esta sintaxis en un archivo DLL, no podrá cargar el archivo DLL explícitamente mediante [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) en versiones de Windows anteriores a Windows Vista. Si el archivo DLL se va a cargar explícitamente, debe usar las funciones de almacenamiento local para el subproceso en lugar de **\_ declspec (Thread)**.

 

 
