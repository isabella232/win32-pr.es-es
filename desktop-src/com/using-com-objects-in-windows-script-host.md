---
title: Usar objetos COM en Windows Script Host
description: Microsoft Windows Script Host es una utilidad de scripting que puede usar para ejecutar scripts en el sistema operativo base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cb28fc0e388ba69f28c56e780d058d27f9e165
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103820471"
---
# <a name="using-com-objects-in-windows-script-host"></a>Usar objetos COM en Windows Script Host

Microsoft Windows Script Host es una utilidad de scripting que puede usar para ejecutar scripts en el sistema operativo base. Puede usar Windows Script Host para automatizar las tareas comunes y crear macros eficaces y scripts de inicio de sesión. Windows Script Host incluye los motores de scripting de VBScript y JScript ActiveX. Otras compañías de software proporcionan motores de scripting ActiveX para lenguajes como PerlScript, PScript, Python y otros.

Para usar un objeto COM en un script ejecutado por Windows Script Host, primero debe crear una instancia del objeto. Después de crear un objeto COM, puede usarlo en scripts.

Windows Script Host se compone de dos aplicaciones. Una ejecuta scripts desde el escritorio de Windows ( `WScript.exe` ); el otro ejecuta scripts desde el símbolo del sistema ( `CScript.exe` ).

Para ejecutar un script desde el escritorio, simplemente haga doble clic en un archivo de script. Los archivos de script son archivos de texto. Por Convención, los archivos de VBScript tienen la extensión `.vbs` y los archivos JScript `.js` .

Para ejecutar un script desde el símbolo del sistema, ejecute la `Cscript.exe` aplicación con una línea de comandos como la siguiente:

```console
cscript "c:\\sample scripts\\chart.vbs"
```

donde `c:\\sample scripts\\chart.vbs` es la ruta de acceso al archivo que contiene el script.

Puede imprimir una lista de los parámetros admitidos por Cscript.exe escribiendo la siguiente línea de comandos:

```console
call cscript //?
```

Para usar un objeto COM en un script ejecutado por Windows Script Host, primero debe crear una instancia del objeto. En VBScript puede hacerlo llamando al `CreateObject()` método. En JScript, puede utilizar el `ActiveXObject` objeto o el `WScript.CreateObject()` método. En el ejemplo siguiente se muestra cómo llamar a `CreateObject()` mediante VBScript:


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



En el ejemplo siguiente se muestra cómo crear un `ActiveXObject` objeto mediante JScript:


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
También puede usar el `WScript.CreateObject()` método en JScript:

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


Después de crear una instancia del objeto COM, puede escribir un script que utilice el objeto, por ejemplo:


```VB
objXL.Visible = true;
 
```



Además del método CreateObject y el objeto ActiveXObject, tanto VBScript como JScript proporcionan el método GetObject, que devuelve una instancia de objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting con objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




