---
title: Compilar marcado de cinta
description: Para que el marco de la cinta de opciones de Windows consuma el archivo de marcado de la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Cinta de Windows, compilar marcado
- Cinta, compilar marcado
- Cinta de Windows, flujo de trabajo del compilador
- Cinta, flujo de trabajo del compilador
- Cinta de Windows, compilador de comandos de la interfaz de usuario (UICC.exe)
- Cinta, compilador de comandos de la interfaz de usuario (UICC.exe)
- Compilador de comandos de IU (UICC.exe)
- UICC.exe (compilador de comandos de IU)
- compilar el marcado de la cinta de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f671e03d7d3a941f1c97891d87c170e65e326d70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532332"
---
# <a name="compiling-ribbon-markup"></a>Compilar marcado de cinta

Para que el marco de la cinta de opciones de Windows consuma el archivo de marcado de la [cinta](windowsribbon-schema.md) de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario. Un compilador de marcado dedicado, el compilador de comandos de la interfaz de usuario (UICC), se incluye con el kit de desarrollo de software (SDK) de Windows (7,0 o posterior) para este propósito. Además de compilar la versión binaria del marcado, UICC genera un archivo de encabezado de definición de identificador (. h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (. RC) que se usa para vincular los recursos de imagen y de cadena a la aplicación host en tiempo de compilación.

-   [Flujo de trabajo compilador](#compiler-workflow)
-   [Sintaxis de línea de comandos](#command-line-syntax)
    -   [Argumentos y opciones](#arguments-and-options)
    -   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="compiler-workflow"></a>Flujo de trabajo compilador

El flujo de trabajo del compilador de marcado de la cinta se muestra en el diagrama siguiente.

![diagrama que muestra el flujo de trabajo del compilador de marcado de cinta.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Sintaxis de línea de comandos

En el ejemplo siguiente se muestra la sintaxis de línea de comandos para el compilador de marcado de la cinta de opciones.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argumentos y opciones

En la tabla siguiente se describen los argumentos y las opciones de esta herramienta.

> [!Note]  
> Las opciones de línea de comandos que se muestran deben especificarse en el orden especificado.

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opción</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>encabezado<headerFile></td>
<td>Genere un archivo de encabezado denominado <headerFile> que contenga los símbolos de recursos de identificador de comando de marcado. Si se omite, no se genera un archivo de encabezado.</td>
</tr>
<tr class="even">
<td>/res<resourceFile></td>
<td>Genere un archivo de recursos denominado <resourceFile> que vincule todos los recursos de imagen y cadena, el archivo de marcado binario y el archivo de encabezado a la aplicación host en tiempo de compilación. Si se omite, no se genera un archivo de recursos.</td>
</tr>
<tr class="odd">
<td>/Name<ribbonName></td>
<td>Nombre del recurso para el archivo de marcado binario registrado en el <resourceFile> . El valor predeterminado es APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtre los mensajes de eventos en función de la gravedad. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Solo mensajes de error.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Solo mensajes de error y ADVERTENCIA.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Predeterminada. <br/> Mensajes de error, de advertencia e informativos.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo utilizar el compilador de marcado de la cinta de opciones para generar un conjunto típico de archivos de recursos para una aplicación de cinta.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declarar comandos y controles con el marcado de la cinta de opciones](windowsribbon-schema.md)
</dt> <dt>

[Crear una aplicación de cinta](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





