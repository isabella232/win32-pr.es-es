---
title: Importar archivos y bibliotecas de tipos
description: Las palabras clave MIDL incluyen, importar e importarlib permiten reutilizar el código haciendo referencia a archivos existentes de encabezado, IDL y lenguaje de definición de objetos (ODL) y bibliotecas de tipos compiladas.
ms.assetid: b4571c1d-4bd7-4ab1-9ef6-14356a6c4bb4
keywords:
- Lenguaje de definición de interfaz de Microsoft MIDL, tareas, importación de archivos y bibliotecas de tipos
- importar MIDL
- bibliotecas de tipos MIDL, importar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b740f29726c1ce4d401fc69b2ea07e811eac0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159538"
---
# <a name="importing-files-and-type-libraries"></a>Importar archivos y bibliotecas de tipos

Las palabras clave MIDL incluyen [**,**](include.md) [**import**](import.md)e [**importlib**](importlib.md) permiten reutilizar el código haciendo referencia a archivos existentes de encabezado, IDL y lenguaje de definición de objetos (ODL) y bibliotecas de tipos compiladas.

La directiva [**include de**](include.md) ACF permite especificar en un archivo ACF uno o varios archivos de encabezado del lenguaje C que se incluirán en el código auxiliar generado por MIDL. El archivo generado tendrá una línea con una directiva **\# include** C-preprocessor con el archivo de encabezado indicado. Use esta **directiva include** para incluir archivos de encabezado específicos de un entorno operativo determinado y que no contengan la información necesaria para la interfaz entre el cliente y el servidor. No use **include para** los archivos de encabezado que contienen tipos de datos que desea que estén disponibles para el archivo IDL; en su lugar, use la [**directiva import.**](import.md)

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

La directiva de [**importación**](import.md) de IDL es el método estándar para incorporar definiciones de tipo e interfaz de otros archivos IDL (o ODL) y archivos de encabezado en el archivo IDL. Todas las instrucciones IDL del archivo importado, como definiciones de tipo, declaraciones [**const**](const.md) y definiciones de interfaz, están disponibles para el archivo IDL de importación.

Al igual que la directiva de preprocesador del lenguaje C incluye **\# ,** la directiva [**import**](import.md) indica al compilador que incluya los tipos de datos definidos en los archivos IDL importados. A diferencia **\# de la directiva include,** **la directiva import** omite los prototipos de procedimiento, ya que no se generan códigos auxiliares para nada en el archivo importado. Dado que el preprocesador se invoca por separado para el archivo importado, las directivas de preprocesador (como **) no se llevan al archivo IDL de importación.

Para obtener información adicional sobre el uso [**de import para**](import.md) incluir archivos de encabezado del sistema en un archivo IDL, vea [Importing System Header Files](importing-system-header-files.md).

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

La directiva [**importlib de**](importlib.md) ODL permite hacer referencia a una biblioteca de tipos compilada en el archivo IDL o ODL. La **directiva importlib** debe estar dentro de una [**instrucción library**](library.md) y debe preceder a otras descripciones de tipos de la biblioteca. La biblioteca importada, así como la biblioteca generada, deben estar disponibles para la aplicación en tiempo de ejecución.

## <a name="example-3"></a>Ejemplo 3

``` syntax
library NewBrowser
{
  importlib("stdole32.tlb");
  importlib("legacy.tlb");
  //remainder of library definition
};
```

También puede usar la directiva **\#** include del preprocesador de C para incluir encabezados y otros archivos en el archivo IDL o ODL. Sin embargo, tenga en cuenta que esta directiva incluirá literalmente todo el contenido del archivo especificado. Si un archivo de encabezado contiene prototipos que no necesita o desea en los archivos de código auxiliar generados por MIDL, o si contiene definiciones de tipo no actualizables, debe usar la directiva de importación [**MIDL**](import.md) en lugar de la **\# directiva include.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Importación**](import.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**incluír**](include.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> </dl>

 

 




