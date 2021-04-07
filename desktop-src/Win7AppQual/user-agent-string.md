---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Cadena del agente de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003203"
---
# <a name="user-agent-string"></a>Cadena del agente de usuario

La *cadena de agente de usuario* contiene información sobre la identidad de un explorador. La cadena de agente de usuario se envía al servidor web como un encabezado HTTP cada vez que un explorador realiza una solicitud a un servidor Web. También puede tener acceso a ella a través de un script del lado cliente. Por ejemplo, puede mostrar la cadena de agente de usuario escribiendo la siguiente dirección URL en la barra de direcciones de Windows Internet Explorer 8: "JavaScript: Alert (Navigator. userAgent)". En la ilustración siguiente se muestra el cuadro de diálogo resultante típico de Internet Explorer 8 que se ejecuta en Windows 7.

![captura de pantalla del cuadro diaog de Internet Explorer que tiene la cadena de agente de usuario](images/useragent-alert.png)

Normalmente, la cadena de agente de usuario se analiza específicamente para la subcadena MSIE. En función de la versión de detectada del explorador, la lógica de programación del lado cliente o del lado servidor toma una acción diferente. Para obtener más información acerca de la cadena de agente de usuario, consulte [¿qué va a notificar Windows Internet Explorer como User-Agent cadena?](/previous-versions/cc817582(v=msdn.10)) en MSDN Library.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



