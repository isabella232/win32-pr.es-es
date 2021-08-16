---
title: Detección del reproductor
description: Detección del reproductor
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Reproductor de Windows Media en línea, detectar reproductores
- tiendas en línea, detectar reproductores
- tiendas en línea de tipo 1, detectar reproductores
- tiendas en línea de tipo 2, detectar reproductores
- Reproductor de Windows Media en línea, detección de reproductores
- tiendas en línea, detección de reproductores
- tiendas en línea de tipo 1, detección de reproductores
- tiendas en línea de tipo 2, detección de reproductores
- detección de reproductores
- detectar reproductores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d511fc8c14a901c6823715293c5eb621b45762cd5e9fae78d8c4df503a03bf38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863515"
---
# <a name="detecting-the-player"></a>Detección del reproductor

Al crear una página web para su tienda en línea, puede decidir que quiere que los usuarios puedan ver la página en un explorador web o en Reproductor de Windows Media. Puede usar un script ASP para determinar si la página web está hospedada en el reproductor.

El código de ejemplo siguiente recupera el parámetro version de la cadena de consulta url para determinar si la página está hospedada en Reproductor de Windows Media:


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



Tenga en cuenta que el código anterior supone que el parámetro version existe en la cadena de consulta cuando se hospeda en Reproductor de Windows Media. Esto es así para las páginas abiertas por el usuario, pero puede que no sea cierto para las páginas abiertas mediante **External.NavigateTaskPaneURL**. Para que la cadena de consulta de versión exista al navegar mediante programación, debe agregar el parámetro version a la llamada al método o anexar dinámicamente la versión a la dirección URL base del elemento **Navigate** del documento ServiceInfo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




