---
description: Asignación de nombres a los buzones y colocación de mensajes en los buzones.
ms.assetid: 1ef522a4-9786-427c-a18a-ae1f0a05cc50
title: Nombres de buzón de correo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf03718a7e603fe891e00d82c2b0b06fab63f8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808414"
---
# <a name="mailslot-names"></a>Nombres de buzón de correo

Cuando un proceso crea un buzón de correo, el nombre del buzón de correo debe tener el formato siguiente.

\\\\.\\ nombre de \\ \[ *ruta de acceso* \\ \]  de buzón

Un nombre de buzón de correo requiere los siguientes elementos: dos barras diagonales inversas para comenzar el nombre, un punto, una barra diagonal inversa después del punto, la palabra "buzón de correo" y una barra diagonal inversa final. Los nombres no distinguen mayúsculas de minúsculas. Un nombre de buzón de correo puede ir precedido de un trazado que consta de los nombres de uno o varios directorios, separados por barras diagonales inversas. Por ejemplo, si un usuario espera mensajes en el asunto de los impuestos de Bob, Ana y Sue, la aplicación de buzón de correo del usuario podría permitir al usuario crear buzones de correo individuales para cada remitente, como se muestra aquí:<dl> \\\\.\\ \\comentarios de \\ bobs de impuestos de buzón de correo \_  
\\\\.\\ Comentarios de los Pedro de los impuestos de buzón de correo \\ \\ \_  
\\\\.\\ \\comentarios de \\ usa de impuestos de buzón de correo \_  
</dl>

Para colocar un mensaje en un buzón de correo, un proceso abre un buzón de correo por nombre. Para escribir en un buzón de correo en el equipo local, un proceso puede usar un nombre de buzón de correo que tenga el mismo formato que se usa para crear un buzón de correo. Sin embargo, esta situación es relativamente poco frecuente. Con más frecuencia, usaría el siguiente formato para escribir en un buzón de correo en un equipo remoto específico:

\\\\*Nombre del equipo* \\ nombre de \\ \[ *ruta de acceso* \\ \]  de buzón

Para colocar un mensaje en cada buzón de correo del dominio especificado con un nombre determinado, use el formato siguiente:

\\\\*Dominio* \\ de nombre de \\ \[ *ruta de acceso* \\ \]  de buzón

Para colocar un mensaje en cada buzón de correo con un nombre determinado en el dominio principal del sistema, utilice el formato siguiente:

\\\\\*\\nombre de \\ \[ *ruta de acceso* \\ \]  de buzón

 

 



