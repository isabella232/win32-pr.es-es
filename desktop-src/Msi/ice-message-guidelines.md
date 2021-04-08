---
description: Las acciones personalizadas de ICE se comunican llamando a MsiProcessMessage y publicando un \_ mensaje de tipo de usuario INSTALLMESSAGE.
ms.assetid: 36307589-de0e-4eaf-b439-e7ba3cd96fb3
title: Instrucciones de mensajes de ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4bee7dbf22184883e49da4d5a5f66f9debb577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001101"
---
# <a name="ice-message-guidelines"></a>Instrucciones de mensajes de ICE

Las acciones personalizadas de ICE se comunican llamando a [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) y publicando un \_ mensaje de tipo de usuario INSTALLMESSAGE.

Al crear una cadena de mensaje para una acción personalizada ICE, dé formato a la cadena como se indica a continuación.

*Nombre de ICE* <tab> *Tipo* <tab> de mensaje *Descripción* <tab> de *Dirección URL o ubicación* <tab> de la ayuda *Nombre* <tab> de tabla *Nombre* <tab> de columna *Clave principal* <tab> *Clave principal* <tab> *Clave principal* . . . (se repite para tantas claves principales como sea necesario)

Los tres primeros campos de la cadena son obligatorios en todos los mensajes.

El campo tipo de mensaje especifica si el ICE informa de un error, un error, una advertencia o un mensaje informativo.



| Value | Tipo de mensaje                                                                                                                                                          |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Mensaje de error que informa del error de la acción personalizada ICE.                                                                                                       |
| 1     | Mensaje de error de creación de base de datos que provoca un comportamiento incorrecto.                                                                                             |
| 2     | Mensaje de advertencia que informa de la creación de bases de datos que provoca un comportamiento incorrecto en ciertos casos. Las advertencias también pueden notificar efectos secundarios inesperados de la creación de bases de datos. |
| 3     | Mensaje informativo.                                                                                                                                                |



 

Si la ayuda no está disponible, el campo dirección URL de ayuda puede ser la cadena vacía.

Los mensajes de error y de advertencia deben proporcionar el nombre de tabla, el nombre de columna y los campos de clave principal. Si se omite alguno de estos campos, todos los campos que siguen al primer campo en blanco deben quedar fuera del mensaje. Por ejemplo, se proporciona un nombre de tabla sin un nombre de columna y claves principales o un nombre de tabla, y se proporciona un nombre de columna sin claves principales. Sin embargo, un nombre de columna y las claves principales no se pueden usar sin un nombre de tabla. Es posible que se muestren varias claves principales hasta que se hayan dado valores a todas las claves principales de la tabla.

## <a name="examples"></a>Ejemplos

El primer mensaje que se muestra [en la ICE de ejemplo en C++](sample-ice-in-c-.md):

"ICE01 \\ T3 \\ Tse ha creado 04/29/1998 by <Insertar aquí el nombre del autor>".

El segundo mensaje publicado por el ICE de ejemplo:

"ICE01 \\ T3 \\ tLast modificó 05/06/1999 por <Insertar aquí el nombre del autor>".

El tercer mensaje publicado por el ICE de ejemplo.

"ICE01 \\ T3 \\ tSimple ICE para ilustrar el concepto de hielo".

 

 



