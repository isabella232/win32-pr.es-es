---
description: Para crear una biblioteca de Dynamic-Link (DLL), debe crear uno o varios archivos de código fuente y, posiblemente, un archivo de vinculador para exportar las funciones.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Creación de la biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12d296b1494cfcedcdfa823eb1a3dd4d408427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811485"
---
# <a name="dynamic-link-library-creation"></a>Creación de la biblioteca Dynamic-Link

Para crear una biblioteca de Dynamic-Link (DLL), debe crear uno o varios archivos de código fuente y, posiblemente, un archivo de vinculador para exportar las funciones. Si planea permitir que las aplicaciones que usan el archivo DLL utilicen la vinculación dinámica en tiempo de carga, también debe crear una biblioteca de importación.

## <a name="creating-source-files"></a>Crear archivos de código fuente

Los archivos de código fuente de un archivo DLL contienen funciones y datos exportados, funciones internas y datos, y una [función de punto de entrada](dynamic-link-library-entry-point-function.md) opcional para el archivo dll. Puede utilizar cualquier herramienta de desarrollo que admita la creación de archivos dll basados en Windows.

Si una aplicación multiproceso puede utilizar la DLL, debe hacer que el archivo DLL sea "seguro para subprocesos". Debe sincronizar el acceso a todos los datos globales del archivo DLL para evitar daños en los datos. También debe asegurarse de que solo vincula las bibliotecas que son seguras para subprocesos. Por ejemplo, Microsoft Visual C++ contiene varias versiones de la biblioteca en tiempo de ejecución de C, una que no es segura para subprocesos y dos que son.

## <a name="exporting-functions"></a>Exportar funciones

La forma en que se especifican las funciones de un archivo DLL debe exportarse depende de las herramientas que se usan para el desarrollo. Algunos compiladores permiten exportar una función directamente en el código fuente utilizando un modificador en la declaración de función. Otras veces, debe especificar las exportaciones en un archivo que se pasa al enlazador.

Por ejemplo, con Visual C++, hay dos formas posibles de exportar funciones DLL: con el modificador [**\_ \_ declspec (dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) o con un archivo de definición de módulo (. def). Si utiliza el modificador **\_ \_ declspec (dllexport)** , no es necesario utilizar un archivo. def. Para obtener más información, vea [exportar desde un archivo dll](/cpp/build/exporting-from-a-dll?view=vs-2019).

## <a name="creating-an-import-library"></a>Crear una biblioteca de importación

Un archivo de biblioteca de importación (. lib) contiene información que el vinculador necesita para resolver las referencias externas a las funciones de DLL exportadas, por lo que el sistema puede localizar la DLL especificada y las funciones de DLL exportadas en tiempo de ejecución. Puede crear una biblioteca de importación para el archivo DLL al compilar el archivo DLL.

Para obtener más información, vea [crear una biblioteca de importación y un archivo de exportación](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).

## <a name="using-an-import-library"></a>Uso de una biblioteca de importación

Por ejemplo, para llamar a la función [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) , debe vincular el código con la biblioteca de importación user32. lib. La razón es que **CreateWindow** reside en un archivo DLL del sistema denominado User32.dll y user32. lib es la biblioteca de importación que se usa para resolver las llamadas a las funciones exportadas en User32.dll en el código. El vinculador crea una tabla que contiene la dirección de cada llamada de función. Las llamadas a las funciones de un archivo DLL se corregirán cuando se cargue el archivo DLL. Mientras el sistema está inicializando el proceso, carga User32.dll porque el proceso depende de las funciones exportadas en ese archivo DLL y actualiza las entradas de la tabla de direcciones de la función. Todas las llamadas a **CreateWindow** invocan la función exportada desde User32.dll.

Para obtener más información, vea [vincular implícitamente con un archivo dll](/previous-versions/d14wsce5(v=vs.140)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una biblioteca de vínculos dinámicos simple](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
