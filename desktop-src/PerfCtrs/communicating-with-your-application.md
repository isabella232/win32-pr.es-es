---
description: Normalmente, un proveedor proporciona datos en nombre de una aplicación.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicación con la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909749"
---
# <a name="communicating-with-your-application"></a>Comunicación con la aplicación

Normalmente, un proveedor proporciona datos en nombre de una aplicación. Por ejemplo, un servidor puede crear un archivo DLL de rendimiento para proporcionar los datos del contador. La comunicación entre una aplicación y su proveedor varía en lo que se refiere a las aplicaciones en modo de usuario y de modo kernel. Los proveedores se ejecutan en modo de usuario. Debido a esto, las aplicaciones de modo de usuario, como las aplicaciones de impresión y visualización, pueden utilizar cualquier técnica para la comunicación entre procesos, como canalizaciones con nombre, asignación de archivos o RPC. Sin embargo, las aplicaciones de modo kernel deben proporcionar una interfaz IOCTL que devuelva los datos de rendimiento al proveedor.

> [!WARNING]
> No utilice COM como mecanismo IPC. El sistema no puede garantizar el estado de inicialización de COM del subproceso que llama a la interfaz. Por lo tanto, es posible que la DLL no pueda inicializar COM correctamente y recopilar los datos.

 

 

 



