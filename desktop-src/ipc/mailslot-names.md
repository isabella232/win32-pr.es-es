---
description: Asignar nombres a mailslots y colocar mensajes en mailslots.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nombres mailslot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359162"
---
# <a name="mailslot-names"></a>Nombres mailslot

Cuando un proceso crea un mailslot, el nombre mailslot debe tener el siguiente formulario.

\\\\.\\ nombre de ruta de \\ \[ *acceso* \\ \] *mailslot*

Un nombre mailslot requiere los siguientes elementos: dos barras diagonales inversas para comenzar el nombre, un punto, una barra diagonal inversa después del punto, la palabra "mailslot" y una barra diagonal inversa final. Los nombres no distinguen mayúsculas de minúsculas. Un nombre mailslot puede ir precedido de una ruta de acceso formada por los nombres de uno o varios directorios, separados por barras diagonales inversas. Por ejemplo, si un usuario espera mensajes sobre el asunto de los impuestos de Bob, Peter y Sue, la aplicación mailslot del usuario podría permitir al usuario crear mailslots individuales para cada remitente, como se muestra aquí:<dl> \\\\.\\ mailslot \\ taxes \\ bobs \_ comments  
\\\\.\\ mailslot \\ taxes \\ emailslot taxes (comentarios de impuestos de \_ mailslot)  
\\\\.\\ mailslot \\ taxes \\ sues \_ comments  
</dl>

Para colocar un mensaje en un mailslot, un proceso abre un mailslot por nombre. Para escribir en un mailslot en el equipo local, un proceso puede usar un nombre mailslot que tenga el mismo formulario usado para crear un mailslot. Sin embargo, esta situación es relativamente poco común. Con más frecuencia, usaría el siguiente formulario para escribir en un mailslot en un equipo remoto específico:

\\\\*NombreDeEquipo* \\ nombre de ruta de \\ \[ *acceso* \\ \] *mailslot*

Para colocar un mensaje en cada mailslot del dominio especificado con un nombre determinado, use el siguiente formulario:

\\\\*DomainName* \\ nombre de ruta de \\ \[ *acceso* \\ \] *mailslot*

Para colocar un mensaje en cada mailslot con un nombre determinado en el dominio principal del sistema, use el siguiente formulario:

\\\\\*\\nombre de ruta de \\ \[ *acceso* \\ \] *mailslot*

 

 



