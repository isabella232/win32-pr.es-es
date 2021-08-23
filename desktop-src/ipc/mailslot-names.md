---
description: Asignar nombres a mailslots y colocar mensajes en mailslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nombres de Mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f96cc5300b3472abe7d6e824266bd0abd0e7b668e38f9f3462eee3cbf3dfb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716905"
---
# <a name="mailslot-names"></a>Nombres de Mailslot

Cuando un proceso crea un mailslot, el nombre mailslot debe tener el siguiente formulario.

\\\\.\\ nombre de ruta de \\ \[ *acceso de* mailslot \\ \] 

Un nombre mailslot requiere los siguientes elementos: dos barras diagonales inversas para comenzar el nombre, un punto, una barra diagonal inversa después del punto, la palabra "mailslot" y una barra diagonal inversa final. Los nombres no distinguen mayúsculas de minúsculas. Un nombre mailslot puede ir precedido de una ruta de acceso que consta de los nombres de uno o varios directorios, separados por barras diagonales inversas. Por ejemplo, si un usuario espera mensajes sobre el asunto de los impuestos de Bob, Quería y Sue, la aplicación mailslot del usuario podría permitir al usuario crear mailslots individuales para cada remitente, como se muestra aquí:<dl> \\\\.\\ mailslot \\ taxes \\ bobs \_ comments  
\\\\.\\ comentarios de impuestos de mailslot \\ \\ \_  
\\\\.\\ mailslot \\ taxes \\ sues \_ comments  
</dl>

Para colocar un mensaje en un mailslot, un proceso abre un mailslot por nombre. Para escribir en un mailslot en el equipo local, un proceso puede usar un nombre mailslot que tenga el mismo formulario usado para crear un mailslot. Sin embargo, esta situación es relativamente poco común. Con más frecuencia, usaría el siguiente formulario para escribir en un mailslot en un equipo remoto específico:

\\\\*NombreDeEquipo* \\ nombre de ruta de \\ \[ *acceso de* mailslot \\ \] 

Para colocar un mensaje en cada mailslot del dominio especificado con un nombre determinado, use el formato siguiente:

\\\\*DomainName* \\ nombre de ruta de \\ \[ *acceso de* mailslot \\ \] 

Para colocar un mensaje en cada mailslot con un nombre determinado en el dominio principal del sistema, use el formato siguiente:

\\\\\*\\nombre de ruta de \\ \[ *acceso de* mailslot \\ \] 

 

 



