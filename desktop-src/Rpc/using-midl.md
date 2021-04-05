---
title: Usar MIDL
description: Crear y compilar una interfaz de Lenguaje de definición de interfaz de Microsoft (MIDL) y una llamada a procedimiento remoto (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793660"
---
# <a name="using-midl"></a>Usar MIDL

Todas las interfaces de los programas que usan RPC deben definirse en Lenguaje de definición de interfaz de Microsoft (MIDL) y compilarse con el compilador de MIDL. En los siguientes temas se presenta una breve introducción a la creación y compilación de una interfaz MIDL:

-   [Definir una interfaz con MIDL](#defining-an-interface-with-midl)
-   [Compilar un archivo MIDL](#compiling-a-midl-file)

Para obtener una explicación detallada de estos temas, vea [los archivos IDL y ACF](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definir una interfaz con MIDL

Los archivos MIDL son archivos de texto que se pueden crear y editar con un editor de texto. Si genera un UUID para la interfaz, normalmente almacenará la salida en un archivo MIDL de plantilla. Para obtener más información sobre el UUID, consulte [generación de UUID de interfaz](generating-interface-uuids.md).

Todas las interfaces de MIDL tienen el mismo formato. Comienzan con un encabezado que contiene una lista de atributos de interfaz y el nombre de la interfaz. Los atributos se incluyen entre corchetes. El encabezado de la interfaz va seguido de su cuerpo, que se incluye entre llaves. En el ejemplo siguiente se muestra una interfaz simple:

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

Algunos de los atributos que normalmente aparecen en una definición de interfaz MIDL son el UUID y el número de versión de la interfaz. El cuerpo de la definición de interfaz debe contener las declaraciones de procedimiento de todos los procedimientos remotos en la interfaz. También puede contener las declaraciones de tipos de datos y constantes que requiere la interfaz.

Todos los parámetros de las declaraciones de procedimiento remoto se deben declarar como \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ **in**, **out** \] . Estas declaraciones especifican que el programa cliente pasa los datos a un procedimiento remoto, obtiene los datos de un procedimiento remoto o ambos. Para obtener información más detallada sobre las declaraciones de parámetros de interfaz, vea [el cuerpo de la interfaz IDL](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Compilar un archivo MIDL

El compilador MIDL es una herramienta de línea de comandos que se instala automáticamente con el kit de desarrollo de software (SDK) de la plataforma. Para invocarlo en una ventana de comandos, escriba el comando **MIDL**, seguido del nombre de un archivo MIDL, en la línea de comandos. Asegúrese de que el directorio que contiene el compilador MIDL está en la ruta de acceso. En el ejemplo siguiente se muestra su uso:

**MyApp. idl de MIDL**

Tenga en cuenta que no tiene que incluir la extensión si el nombre de archivo tiene la extensión. idl. También puede usar los [modificadores de la línea de comandos](/windows/desktop/Midl/midl-command-line-reference) del compilador MIDL si los inserta entre el comando **MIDL** y el nombre de archivo. Esto se muestra en el ejemplo siguiente:

**/ACF de MIDL MyApp. ACF MyApp. idl**

En este ejemplo, el compilador MIDL se ejecuta utilizando el archivo MyApp. idl como archivo de entrada. El modificador de la línea de comandos **/ACF** indica al compilador que utilice también un archivo de configuración de la aplicación (ACF) para la entrada. Los archivos de configuración de la aplicación se describen con más detalle en [los archivos IDL y ACF](the-idl-and-acf-files.md).

Para obtener información más detallada sobre cómo utilizar el compilador MIDL, vea el [lenguaje de definición de interfaz de Microsoft (MIDL)](/windows/desktop/Midl/midl-start-page), que contiene información sobre los temas siguientes:

-   [Requisitos del preprocesador de C para MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [Consideraciones del compilador de C/C++](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Archivos generados para una interfaz RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Referencia de la línea de comandos de MIDL](/windows/desktop/Midl/midl-command-line-reference)
-   [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Errores y advertencias del compilador de MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 