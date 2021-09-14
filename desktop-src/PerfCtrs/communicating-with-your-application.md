---
description: Normalmente, un proveedor proporciona datos en nombre de una aplicación.
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: Comunicación con la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073900"
---
# <a name="communicating-with-your-application"></a>Comunicación con la aplicación

Normalmente, un proveedor proporciona datos en nombre de una aplicación. Por ejemplo, un servidor podría crear un archivo DLL de rendimiento para proporcionar sus datos de contador. La comunicación entre una aplicación y su proveedor difiere para las aplicaciones en modo de usuario y en modo kernel. Los proveedores se ejecutan en modo de usuario. Debido a esto, las aplicaciones en modo de usuario, como las aplicaciones de impresión y visualización, pueden usar cualquier técnica para la comunicación entre procesos, como canalizaciones con nombre, asignación de archivos o RPC. Sin embargo, las aplicaciones en modo kernel deben proporcionar una interfaz IOCTL que devuelva los datos de rendimiento al proveedor.

> [!WARNING]
> No use COM como mecanismo de IPC. El sistema no puede garantizar el estado de inicialización COM del subproceso que llama a la interfaz . Por lo tanto, es posible que el archivo DLL no pueda inicializar correctamente COM y recopilar los datos.

 

 

 



