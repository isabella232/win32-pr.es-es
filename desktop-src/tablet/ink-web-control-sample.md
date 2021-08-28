---
description: En este ejemplo se muestra cómo crear un control habilitado para lápiz para su uso en un explorador web. El ejemplo toma el ejemplo de formulario de notificaciones automáticas original y lo convierte en un control que se coloca en una página web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Ejemplo de control web ink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe2035028ab622f896489b304ca850db4e25462
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882050"
---
# <a name="ink-web-control-sample"></a>Ejemplo de control web ink

En este ejemplo se muestra cómo crear un control habilitado para lápiz para su uso en un explorador web. El ejemplo toma el ejemplo de [formulario de notificaciones](auto-claims-form-sample.md) automáticas original y lo convierte en un control que se coloca en una página web.

Para obtener más información sobre el uso de la entrada de lápiz en la Web, vea [Ink on the Web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Modificaciones en el ejemplo original Project

Este ejemplo consta de una solución que incluye dos proyectos y un archivo HTML. El primer proyecto, AutoClaims, es un proyecto de biblioteca de controles de Microsoft Visual C \# (un control de usuario). El código fuente de este control es casi idéntico al del ejemplo AutoClaims con dos diferencias:

-   La `AutoClaims` clase de este ejemplo hereda de la clase [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) en lugar de [la clase Form.](/dotnet/api/system.windows.forms.form?view=netcore-3.1)

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   La clase AutoClaims de este ejemplo tiene un método público agregado, que elimina los controles secundarios internos que se usan para `DisposeResources` recopilar la entrada de lápiz. Debe llamar a este método mediante la página web en la que se usa el control cuando esa página termina de usar el control .

## <a name="referencing-the-control-in-html"></a>Hacer referencia al control en HTML

La solución incluye un archivo HTML, default.htm. Este archivo es la página a la que navega el explorador para cargar el control. El archivo contiene una &lt; etiqueta de objeto que hace referencia al control &gt; . También incluye un script al que se llama cuando se descarga la página, como indica la presencia del atributo onload=" " en la `OnUnload()` etiqueta &lt; &gt; body. Esta función llama al método en el control para asegurarse de que todos los recursos `DisposeResources` se liberan correctamente al cerrarse.


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



Observe el formato del valor del atributo classid para la &lt; etiqueta de &gt; objeto. Denomina el ensamblado, seguido de un separador de signos y, a continuación, el espacio de nombres que contiene el control y, a continuación, el nombre \# de clase del control.

Un control de usuario real probablemente incluiría métodos adicionales que se usan para conservar o enviar los datos recopilados en la aplicación.

## <a name="the-autoclaims_webcontrol-project"></a>El control WebControl autoclaims \_ Project

El proyecto AutoClaims WebControl es un Project de implementación que crea una instalación que agrega una raíz \_ virtual, AutoClaims WebControl, en el servidor web cuando \_ se instala. El control y el archivo HTML se colocan en esta raíz virtual.

> [!Note]  
> Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK. Debe completar una instalación personalizada y seleccionar la opción "Ejemplos web compilados previamente" para instalarlos.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md)
</dt> <dt>

[Ink on the Web](ink-on-the-web.md)
</dt> </dl>

 

 
