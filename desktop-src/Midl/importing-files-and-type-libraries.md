---
title: Importar archivos y bibliotecas de tipos
description: Las palabras clave de MIDL incluyen, Import y importlib permiten volver a usar el código haciendo referencia a los archivos de encabezado, IDL y lenguaje de definición de objetos (ODL) existentes, y a las bibliotecas de tipos compiladas.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, importar archivos y bibliotecas de tipos
- importar MIDL
- bibliotecas de tipos MIDL, importar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104362397"
---
# <a name="importing-files-and-type-libraries"></a>Importar archivos y bibliotecas de tipos

Las palabras clave de MIDL [**incluyen**](include.md), [**Import**](import.md)y [**importlib**](importlib.md) permiten volver a usar el código haciendo referencia a los archivos de encabezado, IDL y lenguaje de definición de objetos (ODL) existentes, y a las bibliotecas de tipos compiladas.

La Directiva de [**inclusión**](include.md) ACF le permite especificar en un archivo ACF uno o más archivos de encabezado del lenguaje C que se incluirán en el código auxiliar generado por MIDL. El archivo generado tendrá una línea con una directiva de **\# inclusión** de C-preprocesador con el archivo de encabezado indicado. Utilice esta directiva **include** para traer archivos de encabezado específicos de un entorno operativo determinado y que no contengan la información necesaria para la interfaz entre el cliente y el servidor. No utilice **include** para los archivos de encabezado que contengan tipos de datos que desee que estén disponibles para el archivo IDL; en su lugar, use la Directiva de [**importación**](import.md) .

## <a name="example-1"></a>Ejemplo 1

``` syntax
[
  auto_handle
] 
interface X86PC
{ 
  include "gendefs.h", "protos.h", "myfile.h"; 
  //interface typdefs and function declarations here
}
```

La Directiva de [**importación**](import.md) de IDL es el método estándar para traer definiciones de tipo y de interfaz de otros archivos IDL (o ODL) y archivos de encabezado en el archivo IDL. Todas las instrucciones IDL del archivo importado, como definiciones de tipo, declaraciones [**const**](const.md) y definiciones de interfaz, pasan a estar disponibles para el archivo IDL de importación.

Como la Directiva de preprocesador de lenguaje C **\# incluye**, la directiva [**Import**](import.md) indica al compilador que incluya los tipos de datos que se definieron en los archivos IDL importados. A diferencia de la directiva **\# include** , la directiva **Import** omite los prototipos de procedimiento, ya que no se genera ningún código auxiliar para nada en el archivo importado. Dado que el preprocesador se invoca por separado para el archivo importado, las directivas de preprocesador (por ejemplo, * *) no se transportan al archivo IDL de importación.

Para obtener información adicional sobre cómo usar [**importar**](import.md) para incluir archivos de encabezado del sistema en un archivo IDL, vea [importar archivos de encabezado del sistema](importing-system-header-files.md).

## <a name="example-2"></a>Ejemplo 2

``` syntax
[
  uuid(. . .), object
] 
interface IKnown : IUnknown
{
  import "base.idl", "unknwn.idl", "helper.idl";
  //remainder of interface definition
}
```

La Directiva ODL [**importlib**](importlib.md) le permite hacer referencia a una biblioteca de tipos compilada en el archivo IDL o ODL. La directiva **importlib** debe estar dentro de una instrucción [**Library**](library.md) y debe preceder a otras descripciones de tipo de la biblioteca. La biblioteca importada, así como la biblioteca generada, deben estar disponibles para la aplicación en tiempo de ejecución.

## <a name="example-3"></a>Ejemplo 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

También puede usar la directiva **\# include** del preprocesador C para incluir encabezados y otros archivos en el archivo IDL o ODL. No obstante, tenga en cuenta que esta directiva incluirá literalmente todo el contenido del archivo especificado. Si un archivo de encabezado contiene prototipos que no necesita o desea en los archivos de código auxiliar generados por MIDL, o si contiene definiciones de tipo no utilizables, debe usar la Directiva de [**importación**](import.md) MIDL en lugar de la directiva **\# include** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**importar**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**inclui**](include.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> </dl>

 

 




