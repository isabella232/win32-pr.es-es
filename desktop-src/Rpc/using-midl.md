---
title: Uso de MIDL
description: Crear y compilar una interfaz Lenguaje de definición de interfaz de Microsoft (MIDL) y llamada a procedimiento remoto (RPC).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ae89a740831fef28ade4c07dc6bbe2b9b68a8a154eb119f47e16b2cb68b325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010753"
---
# <a name="using-midl"></a>Uso de MIDL

Todas las interfaces de los programas que usan RPC deben definirse en Lenguaje de definición de interfaz de Microsoft (MIDL) y compilarse con el compilador MIDL. En los temas siguientes se presenta una breve introducción a la creación y compilación de una interfaz MIDL:

-   [Definición de una interfaz con MIDL](#defining-an-interface-with-midl)
-   [Compilar un archivo MIDL](#compiling-a-midl-file)

Para obtener una explicación detallada de estos temas, vea [The IDL and ACF Files](the-idl-and-acf-files.md).

## <a name="defining-an-interface-with-midl"></a>Definición de una interfaz con MIDL

Los archivos MIDL son archivos de texto que puede crear y editar con un editor de texto. Si genera un UUID para la interfaz, normalmente almacenará la salida en un archivo MIDL de plantilla. Para obtener más información sobre los UUID, vea [Generating Interface UUIDs](generating-interface-uuids.md).

Todas las interfaces de MIDL tienen el mismo formato. Comienzan con un encabezado que contiene una lista de atributos de interfaz y el nombre de la interfaz. Los atributos se incluyen entre corchetes. El encabezado de interfaz va seguido de su cuerpo, que se incluye entre llaves. En el ejemplo siguiente se muestra una interfaz sencilla:

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

Algunos de los atributos que suelen aparecer en una definición de interfaz MIDL son el UUID y el número de versión de la interfaz. El cuerpo de la definición de interfaz debe contener las declaraciones de procedimiento de todos los procedimientos remotos de la interfaz. También puede contener las declaraciones de tipos de datos y constantes que requiere la interfaz .

Todos los parámetros de las declaraciones de procedimiento remoto deben declararse como \[ [**en**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ **en**, **out** \] . Estas declaraciones especifican que el programa cliente pasa datos a un procedimiento remoto, obtiene los datos de un procedimiento remoto o ambos. Para obtener información más detallada sobre las declaraciones de parámetros de interfaz, vea [The IDL Interface Body](the-idl-interface-body.md).

## <a name="compiling-a-midl-file"></a>Compilar un archivo MIDL

El compilador MIDL es una herramienta de línea de comandos que se instala automáticamente con el Kit de desarrollo de software (SDK) de plataforma. Invoquelo en una ventana de comandos escribiendo el **comando midl**, seguido del nombre de un archivo MIDL, en la línea de comandos. Asegúrese de que el directorio que contiene el compilador MIDL está en la ruta de acceso. En el ejemplo siguiente se muestra su uso:

**midl MyApp.idl**

Tenga en cuenta que no es necesario incluir la extensión si el nombre de archivo tiene la extensión .idl. También puede usar los [](/windows/desktop/Midl/midl-command-line-reference) modificadores de línea de comandos del compilador MIDL insertándolos entre el **comando midl** y el nombre de archivo. Esto se muestra en el ejemplo siguiente:

**midl /acf MyApp.acf MyApp.idl**

En este ejemplo, el compilador MIDL se ejecuta con el archivo MyApp.idl como archivo de entrada. El modificador de línea de **comandos /acf** indica al compilador que use también un archivo de configuración de aplicación (ACF) para la entrada. Los archivos de configuración de la aplicación se analizan más exhaustivamente [en Los archivos IDL y ACF](the-idl-and-acf-files.md).

Para obtener información más detallada sobre el uso del compilador midl, vea el Lenguaje de definición de interfaz de Microsoft [(MIDL),](/windows/desktop/Midl/midl-start-page)que contiene información sobre los temas siguientes:

-   [Requisitos de preprocesador de C para MIDL](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [Consideraciones sobre el compilador de C/C++](/windows/desktop/Midl/c-c-compiler-considerations)
-   [Archivos generados para una interfaz RPC](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [Referencia de la línea de comandos de MIDL](/windows/desktop/Midl/midl-command-line-reference)
-   [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference)
-   [Errores y advertencias del compilador MIDL](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 