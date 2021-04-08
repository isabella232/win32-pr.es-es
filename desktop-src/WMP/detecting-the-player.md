---
title: Detección del reproductor
description: Detección del reproductor
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player tiendas en línea, detectar jugadores
- tiendas en línea, detectar jugadores
- tipo 1 tiendas en línea, detección de reproductores
- tipo 2 tiendas en línea, detección de reproductores
- Windows Media Player tiendas en línea, detección del reproductor
- tiendas en línea, detección del reproductor
- tipo 1 almacenes en línea, detección del reproductor
- tipo 2 tiendas en línea, detección del reproductor
- detección del reproductor
- detección de reproductores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994305"
---
# <a name="detecting-the-player"></a>Detección del reproductor

Al crear una página web para la tienda en línea, puede decidir que quiere que los usuarios puedan ver la página en un explorador Web o en Windows Media Player. Puede usar un script de ASP para determinar si la página web está hospedada en el reproductor.

En el código de ejemplo siguiente se recupera el parámetro de versión de la cadena de consulta de dirección URL para determinar si la página se hospeda en Windows Media Player:


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



Tenga en cuenta que en el código anterior se supone que el parámetro Version existe en la cadena de consulta cuando se hospeda en Windows Media Player. Esto es así para las páginas abiertas por el usuario, pero puede que no sea cierto para las páginas abiertas mediante **external. NavigateTaskPaneURL**. Para que la cadena de consulta de la versión exista al navegar mediante programación, debe agregar el parámetro Version a la llamada al método o anexar dinámicamente la versión a la dirección URL base del elemento **Navigate** del documento ServiceInfo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Creación dinámica del documento ServiceInfo**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




