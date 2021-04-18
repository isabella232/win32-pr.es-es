---
description: En este ejemplo se muestra cómo crear un control con tinta habilitada para su uso en un explorador Web. En el ejemplo se toma el ejemplo de formulario de notificaciones automáticas original y se convierte en un control que se coloca en una página web.
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: Ejemplo de control Web de entrada manuscrita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715083"
---
# <a name="ink-web-control-sample"></a>Ejemplo de control Web de entrada manuscrita

En este ejemplo se muestra cómo crear un control con tinta habilitada para su uso en un explorador Web. En el ejemplo se toma el [ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md) original y se convierte en un control que se coloca en una página web.

Para obtener más información sobre el uso de entradas manuscritas en la web, consulte [entrada de lápiz en la web](ink-on-the-web.md).

## <a name="modifications-to-the-original-sample-project"></a>Modificaciones en el proyecto de ejemplo original

Este ejemplo consta de una solución que incluye dos proyectos y un archivo HTML. El primer proyecto, autoclaims, es un \# proyecto de biblioteca de controles de Microsoft Visual C (un control de usuario). El código fuente de este control es casi idéntico al del ejemplo autoclaims con dos diferencias:

-   La `AutoClaims` clase de este ejemplo hereda de la clase [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) en lugar de la clase [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) .

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   La clase autoclaims de este ejemplo tiene un método público agregado, `DisposeResources` que elimina los controles secundarios internos que se usan para recopilar la entrada de lápiz. La página web en la que se usa el control debe llamar a este método cuando la página termina de usar el control.

## <a name="referencing-the-control-in-html"></a>Hacer referencia al control en HTML

La solución incluye un archivo HTML, default.htm. Este archivo es la página a la que navega el explorador para cargar el control. El archivo contiene una <object> etiqueta que hace referencia al control. También incluye un script al que se llama cuando la página se descarga, tal como se indica en la presencia del atributo onload = " `OnUnload()` " en el <body> . Esta función llama al `DisposeResources` método en el control para asegurarse de que todos los recursos se liberan correctamente en el cierre.


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



Observe el formato del valor del atributo classid para la <object> etiqueta. Asigna un nombre al ensamblado, seguido de un \# separador de signo y, a continuación, el espacio de nombres que contiene el control y, a continuación, el nombre de clase del control.

Un control de usuario real probablemente incluye métodos adicionales que se usan para conservar o enviar los datos recopilados en la aplicación.

## <a name="the-autoclaims_webcontrol-project"></a>Proyecto WebControl de autoclaims \_

El \_ proyecto WebControl Webclaims es un proyecto de implementación que crea una configuración que agrega una raíz virtual, \_ WebControl WebControl en el servidor Web cuando está instalado. El control y el archivo HTML se colocan en esta raíz virtual.

> [!Note]  
> Los ejemplos web compilados no se instalan con la opción de instalación predeterminada para el SDK. Debe completar una instalación personalizada y seleccionar la subopción "ejemplos web precompilados" para instalarlas.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ejemplo de formulario de notificaciones automáticas](auto-claims-form-sample.md)
</dt> <dt>

[Entrada manuscrita en la web](ink-on-the-web.md)
</dt> </dl>

 

 
