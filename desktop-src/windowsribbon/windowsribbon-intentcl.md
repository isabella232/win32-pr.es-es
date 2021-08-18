---
title: Compilación del marcado de la cinta de opciones
description: Para que Windows marco de la cinta de opciones consuma el archivo de marcado de la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario.
ms.assetid: ef9fea92-8c67-461d-9d74-2e259e407fb0
keywords:
- Windows Cinta de opciones, compilar marcado
- Cinta de opciones, compilar marcado
- Windows Cinta de opciones, flujo de trabajo del compilador
- Cinta de opciones, flujo de trabajo del compilador
- Windows Ribbon,UI Command Compiler (UICC.exe)
- Ribbon,UI Command Compiler (UICC.exe)
- Compilador de comandos de interfaz de usuario (UICC.exe)
- UICC.exe (compilador de comandos de interfaz de usuario)
- compilar el marcado Windows cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85534a05b3bde59cc2ec0eec482d8c3b47e898d39ad988c595fbac33eb5e9f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932574"
---
# <a name="compiling-ribbon-markup"></a>Compilación del marcado de la cinta de opciones

Para que Windows de la cinta de opciones consuma el archivo de marcado [de](windowsribbon-schema.md) la cinta de opciones, el archivo de marcado debe compilarse en un archivo de recursos de formato binario. Un compilador de marcado dedicado, el compilador de comandos de interfaz de usuario (UICC), se incluye con el Kit de desarrollo de software (SDK) de Windows (7.0 o posterior) para este propósito. Además de compilar la versión binaria del marcado, uicc genera un archivo de encabezado de definición de identificador (.h) que expone todos los elementos de marcado a la aplicación host de la cinta de opciones y un archivo de recursos (.rc) que se usa para vincular recursos de imagen y cadena a la aplicación host en tiempo de compilación.

-   [Flujo de trabajo del compilador](#compiler-workflow)
-   [Sintaxis de la línea de comandos](#command-line-syntax)
    -   [Argumentos y opciones](#arguments-and-options)
    -   [Ejemplo](#example)
-   [Temas relacionados](#related-topics)

## <a name="compiler-workflow"></a>Flujo de trabajo del compilador

El flujo de trabajo del compilador de marcado de la cinta de opciones se ilustra en el diagrama siguiente.

![diagrama que muestra el flujo de trabajo del compilador de marcado de la cinta de opciones.](images/overviews/overviews-intentcl.png)

## <a name="command-line-syntax"></a>Sintaxis de línea de comandos

La sintaxis de línea de comandos para el compilador de marcado ribbon se muestra en el ejemplo siguiente.


```
UICC <ribbonFile> <binaryFile> [options]
```



### <a name="arguments-and-options"></a>Argumentos y opciones

Los argumentos y las opciones de esta herramienta se describen en la tabla siguiente.

> [!Note]  
> Las opciones de línea de comandos enumeradas deben especificarse en el orden especificado.

 



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
<td>/header:<headerFile></td>
<td>Genere un archivo de encabezado llamado <headerFile> que contiene los símbolos de recursos de identificador de comando de marcado. Si se omite, no se genera un archivo de encabezado.</td>
</tr>
<tr class="even">
<td>/res:<resourceFile></td>
<td>Genere un archivo de recursos denominado que vincula todos los recursos de imagen y cadena, el archivo de marcado binario y el archivo de encabezado a la aplicación <resourceFile> host en tiempo de compilación. Si se omite, no se genera un archivo de recursos.</td>
</tr>
<tr class="odd">
<td>/name:<ribbonName></td>
<td>Nombre del recurso para el archivo de marcado binario que se registra en <resourceFile> . El valor predeterminado es APPLICATION_RIBBON.</td>
</tr>
<tr class="even">
<td>/W{0\1\2}</td>
<td>Filtre los mensajes de evento en función de la gravedad. 
<table>
<tbody>
<tr class="odd">
<td>0<br/></td>
<td>Solo mensajes de error.<br/></td>
</tr>
<tr class="even">
<td>1<br/></td>
<td>Solo mensajes de error y advertencia.<br/></td>
</tr>
<tr class="odd">
<td><strong>2</strong><br/></td>
<td>Predeterminada. <br/> Mensajes de error, advertencia e informativos.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar el compilador de marcado ribbon para generar un conjunto típico de archivos de recursos para una aplicación de cinta de opciones.

`UICC.exe RibbonMarkup.xml RibbonMarkup.bml /header:RibbonIds.h /res:RibbonUI.rc`

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Declarar comandos y controles con marcado de cinta](windowsribbon-schema.md)
</dt> <dt>

[Crear una aplicación de cinta de opciones](windowsribbon-stepbystep.md)
</dt> </dl>

 

 





