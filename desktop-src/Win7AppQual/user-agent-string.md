---
description: Cadena del agente de usuario
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Cadena del agente de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084183"
---
# <a name="user-agent-string"></a>Cadena del agente de usuario

La *cadena del agente de usuario* contiene información sobre la identidad de un explorador. La cadena del agente de usuario se notifica al servidor web como un encabezado HTTP cada vez que un explorador realiza una solicitud a un servidor web. También puede acceder a él a través de un script del lado cliente. Por ejemplo, puede mostrar la cadena del agente de usuario escribiendo la siguiente dirección URL en la barra de direcciones de Windows Internet Explorer 8: "javascript:alert(navigator.userAgent)". En la ilustración siguiente se muestra el cuadro de diálogo resultante típico de Internet Explorer 8 que se ejecuta en Windows 7.

![captura de pantalla del cuadro de diálogo de Internet Explorer que tiene la cadena del agente de usuario](images/useragent-alert.png)

Normalmente, la cadena del agente de usuario se analiza específicamente para la subcadena MSIE. En función de la versión notificada del explorador, la lógica de programación del lado cliente o del lado servidor realiza una acción diferente. Para obtener más información sobre la cadena del Agente de usuario, vea [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) en MSDN Library.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corrección de problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



