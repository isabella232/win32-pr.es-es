---
description: Cada canalización con nombre tiene un nombre único que la distingue de otras canalizaciones con nombre en la lista de sistemas de objetos con nombre. Un servidor de canalización especifica un nombre para la canalización cuando llama a la función CreateNamedPipe para crear una o varias instancias de una canalización con nombre.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Nombres de canalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172278"
---
# <a name="pipe-names"></a>Nombres de canalización

Cada canalización con nombre tiene un nombre único que la distingue de otras canalizaciones con nombre en la lista de objetos con nombre del sistema. Un servidor de canalización especifica un nombre para la canalización cuando llama a la función [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para crear una o varias instancias de una canalización con nombre. Los clientes de canalización especifican el nombre de canalización cuando llaman a la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) o [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para conectarse a una instancia de la canalización con nombre.

Use el siguiente formulario al especificar el nombre de una canalización en la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)o [**CallNamedPipe:**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)

\\\\*ServerName* \\ pipe \\ *PipeName*

donde *ServerName* es el nombre de un equipo remoto o un punto, para especificar el equipo local. La cadena de nombre de canalización especificada por *PipeName* puede incluir cualquier carácter que no sea una barra diagonal inversa, incluidos números y caracteres especiales. La cadena de nombre de canalización completa puede tener hasta 256 caracteres. Los nombres de canalización no distinguen mayúsculas de minúsculas.

El servidor de canalización no puede crear una canalización en otro equipo, por lo que [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) debe usar un punto para el nombre del servidor, como se muestra en el ejemplo siguiente.

\\\\.\\ pipe \\ *PipeName*

Un servidor de canalización puede proporcionar el nombre de canalización a sus clientes de canalización para que puedan conectarse a la canalización. El cliente de canalización detecta el nombre de canalización de algún origen persistente, como una entrada del Registro, un archivo u otra aplicación. De lo contrario, los clientes deben conocer el nombre de la canalización en tiempo de compilación.

 

 
