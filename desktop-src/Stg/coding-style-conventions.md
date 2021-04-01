---
title: Convenciones de estilo de codificación
description: Las convenciones de estilo de codificación se usan en esta serie de ejemplo para ayudar a la claridad y coherencia.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797373"
---
# <a name="coding-style-conventions"></a>Convenciones de estilo de codificación

Las convenciones de estilo de codificación se usan en esta serie de ejemplo para ayudar a la claridad y coherencia. Se usan las convenciones de notación "húngaro". Se han convertido en una práctica de codificación común en la programación de Win32. Incluyen anotaciones de prefijo variables que proporcionan a los nombres de variable una sugerencia del tipo de la variable.

En la tabla siguiente se enumeran los prefijos comunes.



| Prefijo | Descripción                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| CB     | Recuento de bytes                      |
| cr     | Valor de referencia de color               |
| serie     | Recuento de x (corto)                  |
| dw     | DWORD (unsigned Long)               |
| f      | Marcas (normalmente varios valores de bit) |
| fn     | Función                            |
| i\_    | Global                              |
| h      | Handle                              |
| i      | Entero                             |
| l      | long                                |
| lp     | Puntero largo                        |
| f\_    | Miembro de datos de una clase              |
| n      | Short int                           |
| p      | Puntero                             |
| s      | String                              |
| sz     | Cadena terminada en cero              |
| tm     | Métrica de texto                         |
| u      | Unsigned int                        |
| UL     | Unsigned Long (ULONG)               |
| w      | WORD (corto sin signo)               |
| x, y    | coordenadas x, y (cortas)            |



 

A menudo se combinan, como en el siguiente.



| Combinación de prefijo | Descripción                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | Puntero a una cadena.                                  |
| m \_ pszMyString     | Puntero a una cadena que es un miembro de datos de una clase. |



 

En la tabla siguiente se enumeran otras convenciones.



| Convención       | Descripción                                              |
|------------------|----------------------------------------------------------|
| CMyClass         | Prefijo ' C ' para los nombres de clase de C++.                          |
| COMyObjectClass  | Prefijo ' CO ' para los nombres de clase de objeto COM.                  |
| CFMyClassFactory | Prefijo ' CF ' para los nombres de generador de clases COM.                 |
| IMyInterface     | Prefijo ' I ' para los nombres de clase de interfaz COM.                |
| CImpIMyInterface | Prefijo ' CImpI ' para las clases de implementación de interfaz COM. |



 

En esta serie de ejemplos se usan algunas convenciones coherentes para los bloques de encabezado de comentario, como se indica a continuación.

## <a name="file-header"></a>Encabezado de archivo

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>Bloque de comentario sin formato

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>Encabezado de declaración de clase

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>Encabezado de definición del método de clase

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Función no exportada o local

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>Encabezado de definición de función exportada

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>Encabezado de declaración de interfaz COM

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>Encabezado de declaración de clase de objeto COM

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

Todas estas convenciones de bloque de comentario tienen cadenas de token de inicio y finalización coherentes. Esta coherencia admite el procesamiento automático de los encabezados de alguna manera. Por ejemplo, se pueden escribir scripts de AWK para filtrar los encabezados de función en un archivo de texto independiente que puede servir como base para un documento de especificación. Del mismo modo, las herramientas como la utilidad autoduck no admitida (actualmente disponible en el CD-ROM de la biblioteca de desarrollo de Microsoft Developer Network) se pueden usar para procesar los bloques de comentarios de estos encabezados.

En la tabla siguiente se enumeran las cadenas de token de inicio y finalización usadas en los tutoriales de ejemplo.



| Token | Descripción                      |
|-------|----------------------------------|
| /\*+  | Inicio del encabezado de archivo                |
| +\*/  | Fin del encabezado de archivo                  |
| /\*-  | Inicio de encabezado de bloque de comentario sin formato |
| -\*/  | Final de encabezado de bloque de comentario sin formato   |
| /\*Unidad  | Inicio del encabezado de clase               |
| Unidad\*/  | Fin de encabezado de clase                 |
| /\*F  | Inicio de encabezado de método              |
| F\*/  | Fin del encabezado de método                |
| /\*Formato  | Inicio del encabezado de función            |
| Formato\*/  | Fin del encabezado de función              |
| /\*Configur  | Inicio de encabezado de interfaz           |
| Configur\*/  | Fin de encabezado de interfaz             |
| /\*Aceptar  | Inicio del encabezado de clase de objeto COM    |
| Aceptar\*/  | Fin de encabezado de clase de objeto COM      |



 

Estos encabezados también se pueden usar como indicaciones visuales para el examen rápido de archivos de código fuente. También proporcionan comodidad para obtener rápidamente una ubicación de origen si configura cadenas de búsqueda en el editor y, a continuación, "repetir la última búsqueda" para encontrar rápidamente estos encabezados.

Por ejemplo, la cadena de búsqueda "M + M" buscará el inicio de los encabezados de método y "M-M" buscará el principio del código de implementación o la definición de método real.

 

 




