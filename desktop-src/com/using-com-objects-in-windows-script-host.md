---
title: Uso de objetos COM en Windows host de script
description: Microsoft Windows Script Host es una utilidad de scripting que puede usar para ejecutar scripts en el sistema operativo base.
ms.assetid: b13c1bdf-91ce-42a2-b66a-20d68952bb34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3ba9a14fa948dea9ed716cfa6f3e082d9fb4f56bb3995f052447787ba949a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117917755"
---
# <a name="using-com-objects-in-windows-script-host"></a>Uso de objetos COM en Windows host de script

Microsoft Windows Script Host es una utilidad de scripting que puede usar para ejecutar scripts en el sistema operativo base. Puede usar el host Windows script para automatizar tareas comunes y crear potentes macros y scripts de inicio de sesión. Windows El host de script incluye VBScript JScript ActiveX motores de scripting. Otras empresas de software ActiveX motores de scripting para lenguajes como PerlScript, PScript, Python y otros.

Para usar un objeto COM en un script ejecutado por Windows host de script, primero debe crear una instancia del objeto . Después de crear un objeto COM, puede usarlo en scripts.

Windows El host de script consta de dos aplicaciones. Uno ejecuta scripts desde el Windows escritorio ( `WScript.exe` ); el otro ejecuta scripts desde el símbolo del sistema ( `CScript.exe` ).

Para ejecutar un script desde el escritorio, basta con hacer doble clic en un archivo de script. Los archivos de script son archivos de texto. Por convención, los archivos VBScript tienen la `.vbs` extensión y JScript archivos `.js` .

Para ejecutar un script desde el símbolo del sistema, ejecute la aplicación con una línea de `Cscript.exe` comandos como la siguiente:

```console
cscript "c:\\sample scripts\\chart.vbs"
```

donde `c:\\sample scripts\\chart.vbs` es la ruta de acceso al archivo que contiene el script.

Puede imprimir una lista de los parámetros admitidos por Cscript.exe especificando la siguiente línea de comandos:

```console
call cscript //?
```

Para usar un objeto COM en un script ejecutado por Windows host de script, primero debe crear una instancia del objeto . En VBScript, puede hacerlo llamando al `CreateObject()` método . En JScript se puede usar el `ActiveXObject` objeto o el método `WScript.CreateObject()` . En el ejemplo siguiente se muestra cómo `CreateObject()` llamar a mediante VBScript:


```VB
Dim objXL
Set objXL = CreateObject("Excel.Application")
 
```



En el ejemplo siguiente se muestra cómo crear `ActiveXObject` un objeto mediante JScript:


```JScript
var objXL = new ActiveXObject("Excel.Application");
 
```
También puede usar `WScript.CreateObject()` el método dentro de JScript:

```JScript
var objXL = WScript.CreateObject("Excel.Application");
```


Después de crear una instancia del objeto COM, puede escribir un script que use el objeto , por ejemplo:


```VB
objXL.Visible = true;
 
```



Además del método CreateObject y el objeto ActiveXObject, tanto VBScript como JScript proporcionan el método GetObject, que devuelve una instancia de objeto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Scripting con objetos COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




