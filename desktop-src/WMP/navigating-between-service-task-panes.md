---
title: Desplazarse entre los paneles de tareas de servicio
description: Desplazarse entre los paneles de tareas de servicio
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Windows Media Player tiendas en línea, navegar
- tiendas en línea, navegar
- Escriba 2 tiendas en línea, navegación
- Windows Media Player tiendas en línea, paneles de tareas de servicio
- tiendas en línea, paneles de tareas de servicio
- tipo 2 tiendas en línea, paneles de tareas de servicio
- Windows Media Player tiendas en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tipo 2 tiendas en línea, paneles de tareas
- navegar por las tiendas en línea de tipo 2
- Media Player de Windows, paneles de tareas de servicio
- Media Player de Windows, paneles de tareas
- paneles de tareas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86035215f822c67bb40c528f141422977efc8653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357098"
---
# <a name="navigating-between-service-task-panes"></a>Desplazarse entre los paneles de tareas de servicio

Para desplazarse entre los paneles de tareas de servicio de Windows Media Player, use el método **NavigateTaskPaneURL** , que está disponible mediante el objeto **window. external** . Cuando se usa este método, se especifican valores para tres parámetros:

-   *bstrKeyName*. Este es el nombre de la clave de la tienda en línea. Al navegar en una tienda en línea, use el nombre de clave del almacén actual.
-   *bstrTaskPane*. Esta cadena contiene el nombre del panel de tareas de servicio al que desea desplazarse.
-   *bstrParams*. Esta cadena contiene los parámetros de cadena de consulta que desea anexar a la dirección URL de la página web hospedada por el panel de tareas de servicio al que desea desplazarse.

La navegación se administra mediante una página web que se crea, denominada página navegar. La dirección URL de la página navegar se especifica mediante el elemento **Navigate** del documento ServiceInfo. Cuando se llama a **NavigateTaskPaneURL**, Windows Media Player abre la página navegar, no la Página Web especificada por los elementos **ServiceTask1**, **ServiceTask2** o **ServiceTask3** . Es la página de navegación que recibe la cadena de consulta especificada por *bstrParams*. La página navegar debe contener las reglas que determinan el contenido que se muestra en un panel de tareas de servicio después de la navegación.

Por ejemplo, supongamos que quiere que los usuarios haga clic en un vínculo para navegar de **ServiceTask1** a **ServiceTask2**. Puede usar el siguiente código HTML para crear el vínculo:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Cuando el usuario hace clic en el vínculo de vídeo, Windows Media Player cambia a **ServiceTask2** y abre la página navegar, anexando la siguiente cadena de consulta a su dirección URL.


```C++
?From=Music&To=2

```



El parámetro from identifica la página desde la que el usuario hizo clic en el vínculo y el parámetro to identifica el número del panel de tareas de servicio al que desea navegar. (Tenga en cuenta que no hay nada especial sobre estos parámetros. Puede usar los parámetros que desee para cualquier propósito que elija).

Por ejemplo, en el ejemplo de código siguiente se muestra el elemento **Navigate** en un documento ServiceInfo:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



La dirección URL resultante, completa con la cadena de consulta, se muestra en el ejemplo siguiente:


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



En el ejemplo de código siguiente se muestra la página navegar:


```C++
<%
    Dim sURL
    Dim sQS
    Dim sTo

    sURL = ""
    sQS = Request.ServerVariables("QUERY_STRING")
    sTo = "" & Request.QueryString("To")
 
    Select Case sTo
       Case "1" sURL = sURL & "Music_Music.asp"
       Case "2" sURL = sURL & "Music_Video.asp"
       Case "3" sURL = sURL & "Music_Radio.asp"
       Case Else sURL = sURL & "Music_Music.asp"
    End Select
     
    sURL = sURL & "?" & sQS

    Response.Redirect(sURL)    
%>

```



El código anterior simplemente crea una dirección URL y redirige el explorador a ella. En primer lugar, el código recupera los valores de la cadena de consulta de la dirección URL y la propia cadena de consulta. Usa el valor del parámetro to para determinar la página que se va a mostrar. A continuación, anexa la cadena de consulta original a la dirección URL. Por último, navega por el explorador con una dirección URL similar a la siguiente:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Siempre que realice la navegación de esta manera, asegúrese de especificar [external. SelectedTaskPane](external-selectedtaskpane.md) para asegurarse de que el botón de tarea correcto esté resaltado.

-   **ADVERTENCIA** de Tenga cuidado con el uso de parámetros de cadena de consulta para la navegación.

Cualquier persona que cree una lista de reproducción de ASX puede proporcionar páginas web HTMLView. Esto significa que los sitios Web malintencionados pueden pasar valores de cadena de consulta a la tienda en línea mediante **NavigateTaskPaneURL**. Debe planear esta posibilidad para proteger la tienda en línea. Por ejemplo, si la tienda en línea simplemente muestra un valor de cadena de consulta para el usuario, un sitio Web malintencionado podría mostrar texto inesperado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento Navigate**](navigate-element.md)
</dt> <dt>

[**Navegación para las tiendas en línea de tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




