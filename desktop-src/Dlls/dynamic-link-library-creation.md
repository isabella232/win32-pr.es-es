---
description: Para crear una biblioteca Dynamic-Link (DLL), debe crear uno o varios archivos de código fuente y, posiblemente, un archivo de vinculador para exportar las funciones.
ms.assetid: b66ea0e8-84c3-40be-bf02-765b9dd61f9f
title: Dynamic-Link de bibliotecas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89047e24fe61483b3ac807b59abc114206a00f9df18566b5fb02947268fbd792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650455"
---
# <a name="dynamic-link-library-creation"></a>Dynamic-Link de bibliotecas

Para crear una biblioteca Dynamic-Link (DLL), debe crear uno o varios archivos de código fuente y, posiblemente, un archivo de vinculador para exportar las funciones. Si tiene previsto permitir que las aplicaciones que usan el archivo DLL usen la vinculación dinámica en tiempo de carga, también debe crear una biblioteca de importación.

## <a name="creating-source-files"></a>Crear archivos de origen

Los archivos de origen de un archivo DLL contienen funciones y datos exportados, funciones internas y datos, y una función de punto de entrada [opcional](dynamic-link-library-entry-point-function.md) para el archivo DLL. Puede usar cualquier herramienta de desarrollo que admita la creación de archivos DLL Windows basados en archivos DLL.

Si una aplicación multiproceso puede usar el archivo DLL, debe hacer que el archivo DLL sea "seguro para subprocesos". Debe sincronizar el acceso a todos los datos globales del archivo DLL para evitar daños en los datos. También debe asegurarse de vincular solo con bibliotecas que también son seguras para subprocesos. Por ejemplo, Microsoft Visual C++ contiene varias versiones de la biblioteca en tiempo de ejecución de C, una que no es segura para subprocesos y dos que sí.

## <a name="exporting-functions"></a>Exportar funciones

La forma de especificar qué funciones de un archivo DLL se deben exportar depende de las herramientas que se usan para el desarrollo. Algunos compiladores permiten exportar una función directamente en el código fuente mediante un modificador en la declaración de función. Otras veces, debe especificar exportaciones en un archivo que pase al vinculador.

Por ejemplo, mediante Visual C++, hay dos maneras posibles de exportar funciones DLL: con el modificador [**\_ \_ declspec(dllexport)**](https://msdn.microsoft.com/library/3y1sfaz2(v=VS.71).aspx) o con un archivo module-definition (.def). Si usa el **\_ \_ modificador declspec(dllexport),** no es necesario usar un archivo .def. Para obtener más información, [vea Exportar desde un archivo DLL.](/cpp/build/exporting-from-a-dll?view=vs-2019)

## <a name="creating-an-import-library"></a>Crear una biblioteca de importación

Un archivo de biblioteca de importación (.lib) contiene información que el vinculador necesita para resolver las referencias externas a las funciones DLL exportadas, de modo que el sistema pueda encontrar el archivo DLL especificado y las funciones DLL exportadas en tiempo de ejecución. Puede crear una biblioteca de importación para el archivo DLL al compilar el archivo DLL.

Para obtener más información, vea [Compilar una biblioteca de importación y Exportar archivo](/cpp/build/reference/building-an-import-library-and-export-file?view=vs-2019).

## <a name="using-an-import-library"></a>Uso de una biblioteca de importación

Por ejemplo, para llamar a [**la función CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) debe vincular el código con la biblioteca de importación User32.lib. El motivo es que **CreateWindow** reside en un archivo DLL del sistema denominado User32.dll y User32.lib es la biblioteca de importación que se usa para resolver las llamadas a funciones exportadas en User32.dll en el código. El vinculador crea una tabla que contiene la dirección de cada llamada de función. Las llamadas a funciones de un archivo DLL se solucionarán cuando se cargue el archivo DLL. Mientras el sistema inicializa el proceso, carga User32.dll porque el proceso depende de las funciones exportadas en ese archivo DLL y actualiza las entradas de la tabla de direcciones de función. Todas las llamadas **a CreateWindow** invocan la función exportada desde User32.dll.

Para obtener información, [vea Vincular implícitamente con un archivo DLL.](/previous-versions/d14wsce5(v=vs.140))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una biblioteca de vínculos dinámicos simple](creating-a-simple-dynamic-link-library.md)
</dt> <dt>

[DLL (Visual C++)](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
