---
title: Navegar entre paneles de tareas de servicio
description: Navegar entre paneles de tareas de servicio
ms.assetid: cb26a26d-a80d-4af5-9c5f-fab01129d83c
keywords:
- Reproductor de Windows Media en línea, navegar
- tiendas en línea, navegar
- tiendas en línea de tipo 2, navegar
- Reproductor de Windows Media en línea, paneles de tareas de servicio
- tiendas en línea, paneles de tareas de servicio
- tipo 2 tiendas en línea, paneles de tareas de servicio
- Reproductor de Windows Media en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tiendas en línea de tipo 2, paneles de tareas
- navegar por las tiendas en línea de tipo 2
- Reproductor de Windows Media, paneles de tareas de servicio
- Reproductor de Windows Media,paneles de tareas
- paneles de tareas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f54a82f2637fe11b0a2a7703cc241c47e799999a89b56ba8ba19c079b7393de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647585"
---
# <a name="navigating-between-service-task-panes"></a>Navegar entre paneles de tareas de servicio

Para navegar entre los paneles de tareas del servicio Reproductor de Windows Media, use el método **NavigateTaskPaneURL,** que está disponible mediante el **objeto window.external.** Cuando se usa este método, se especifican valores para tres parámetros:

-   *bstrKeyName*. Este es el nombre de clave de la tienda en línea. Al navegar dentro de un almacén en línea, use el nombre de clave del almacén actual.
-   *bstrTaskPane*. Esta cadena contiene el nombre del panel de tareas de servicio al que desea navegar.
-   *bstrParams*. Esta cadena contiene los parámetros de cadena de consulta que desea anexar a la dirección URL de la página web hospedada por el panel de tareas de servicio al que desea navegar.

La navegación se administra mediante una página web que se crea, denominada página de navegación. El elemento Navigate del documento ServiceInfo especifica la dirección URL de la página de navegación.  Cuando se llama a **NavigateTaskPaneURL**, Reproductor de Windows Media abre la página de navegación, no la página web especificada por los elementos **ServiceTask1,** **ServiceTask2** o **ServiceTask3.** Es la página de navegación la que recibe la cadena de consulta especificada por *bstrParams.* La página de navegación debe contener las reglas que determinan qué contenido se muestra en un panel de tareas de servicio después de la navegación.

Por ejemplo, supongamos que quiere que los usuarios haga clic en un vínculo para navegar de **ServiceTask1** a **ServiceTask2.** Puede usar el siguiente código HTML para crear el vínculo:


```C++
<A HREF = "javascript:window.external.NavigateTaskPaneURL('MSSampleMusic', 'ServiceTask2', 'From=Music&To=2')">Video</A>

```



Cuando el usuario hace clic en el vínculo Vídeo, Reproductor de Windows Media cambia a **ServiceTask2** y abre la página de navegación, anexando la siguiente cadena de consulta a su dirección URL.


```C++
?From=Music&To=2

```



El parámetro From identifica la página desde la que el usuario hizo clic en el vínculo y el parámetro To identifica el número del panel de tareas de servicio al que desea navegar. (Tenga en cuenta que no hay nada especial sobre estos parámetros. Puede usar los parámetros que quiera para cualquier propósito que elija).

Por ejemplo, el código de ejemplo siguiente muestra **el elemento Navigate** en un documento ServiceInfo:


```C++
<Navigate
        BaseURL = "https://www.proseware.com/service/html/navigate.asp">
```



La dirección URL resultante, completa con la cadena de consulta, se muestra en el ejemplo siguiente:


```C++
https://www.proseware.com/service/html/navigate.asp?From=Music&To=2

```



El código de ejemplo siguiente muestra la página de navegación:


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



El código anterior simplemente crea una dirección URL y redirige el explorador a ella. En primer lugar, el código recupera los valores To de la cadena de consulta url y la propia cadena de consulta. Usa el valor del parámetro To para determinar qué página se va a mostrar. A continuación, anexa la cadena de consulta original a la dirección URL. Por último, navega por el explorador mediante una dirección URL similar a la siguiente:


```C++
https://www.proseware.com/service/html/Video.asp?locale=409&geoid=f4&version=10.0.0.3600&userlocale=409&From=Music&To=2

```



Siempre que realice la navegación de esta manera, asegúrese de especificar [External.SelectedTaskPane](external-selectedtaskpane.md) para asegurarse de que el botón de tarea correcto está resaltado.

-   **Advertencia** Tenga cuidado al usar parámetros de cadena de consulta para la navegación.

Cualquiera que cree una lista de reproducción de ASX puede proporcionar páginas web HTMLView. Esto significa que los sitios web malintencionados pueden pasar valores de cadena de consulta a su tienda en línea **mediante NavigateTaskPaneURL**. Debe planear esta posibilidad para mantener la tienda en línea segura. Por ejemplo, si la tienda en línea simplemente muestra un valor de cadena de consulta al usuario, un sitio web malintencionado podría mostrar texto inesperado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento Navigate**](navigate-element.md)
</dt> <dt>

[**Navegación para almacenes en línea de tipo 2**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




