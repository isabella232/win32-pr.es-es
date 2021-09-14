---
description: Las acciones personalizadas de ICE se comunican llamando a MsiProcessMessage y publicando un mensaje de tipo INSTALLMESSAGE \_ USER.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Instrucciones de mensajes ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d603175dbecc12b0b9524db1a02d9ca677f61c87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074692"
---
# <a name="ice-message-guidelines"></a>Instrucciones de mensajes ICE

Las acciones personalizadas de ICE se comunican [**llamando a MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y publicando un mensaje de tipo INSTALLMESSAGE \_ USER.

Al crear una cadena de mensaje para una acción personalizada de ICE, formatee la cadena como se indica a continuación.

*Nombre de ICE* &lt; tab &gt; *Message Type tab Description* tab &lt; &gt; *Help* &lt; URL or &gt; *location* tab &lt; Table &gt; *Name* tab &lt; Column &gt; *Name* tab &lt; Primary &gt; *Key* tab Primary &lt; Key tab Primary &gt; *Key* &lt; tab Primary &gt; *Key* . . . (repita para tantas claves principales como sea necesario)

Los tres primeros campos de la cadena son necesarios en cada mensaje.

El campo Tipo de mensaje especifica si el ICE notifica un mensaje de error, error, advertencia o informativo.



| Value | Tipo de mensaje                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Mensaje de error que informa del error de la acción personalizada de ICE.                                                                                                       |
| 1     | Mensaje de error que informa de la creación de bases de datos que provocan un comportamiento incorrecto.                                                                                             |
| 2     | Mensaje de advertencia que informa de la creación de bases de datos que provoca un comportamiento incorrecto en determinados casos. Las advertencias también pueden notificar efectos secundarios inesperados de la creación de bases de datos. |
| 3     | Mensaje informativo.                                                                                                                                                |



 

Si la ayuda no está disponible, el campo Url de ayuda puede ser la cadena vacía.

Los mensajes de error y advertencia deben proporcionar los campos Nombre de tabla, Nombre de columna y Clave principal. Si se omite cualquiera de estos campos, todos los campos siguientes al primer campo en blanco se deben dejar fuera del mensaje. Por ejemplo, se proporciona un nombre de tabla sin un nombre de columna y claves principales o un nombre de tabla, y se proporciona un nombre de columna sin claves principales. Sin embargo, no se pueden usar un nombre de columna ni claves principales sin un nombre de tabla. Se pueden enumerar varias claves principales hasta que se hayan dado valores a todas las claves principales de esa tabla.

## <a name="examples"></a>Ejemplos

Primer mensaje ilustrado por el [ICE de ejemplo en C++:](sample-ice-in-c-.md)

"ICE01 \\ t3 \\ tCreated 04/29/1998 by <insert author's name here>".

Segundo mensaje publicado por el ICE de ejemplo:

"ICE01 \\ t3 \\ tLast modified 05/06/1999 by <insert author's name here>".

Tercer mensaje publicado por el ICE de ejemplo.

"ICE01 \\ t3 \\ tSimple ICE to illustrating the ICE concept".

 

 



