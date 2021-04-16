---
description: Un protocolo de transporte debe estar instalado correctamente en el sistema y estar registrado en Windows Sockets para ser accesible para una aplicación.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Acceso simultáneo a varios protocolos de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706103"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Acceso simultáneo a varios protocolos de transporte

Un protocolo de transporte debe estar instalado correctamente en el sistema y estar registrado en Windows Sockets para ser accesible para una aplicación. La \_ biblioteca32.dll de Ws2 exporta un conjunto de funciones para facilitar el proceso de registro. Esto incluye la creación de un nuevo registro y la eliminación de uno existente.

Cuando se crean nuevos registros, el autor de la llamada (es decir, el script de instalación del proveedor de la pila) proporciona una o varias estructuras de información de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) rellenadas que contienen un conjunto completo de información sobre el protocolo. Para obtener más información, vea [Windows Sockets 2 SPI](about-the-winsock-spi.md). Cualquier pila de transporte instalada de esta manera se conoce como proveedor de servicios de Windows Sockets.

En Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) y Windows Vista y versiones posteriores. el catálogo Winsock que contiene una lista de proveedores de transporte y de espacio de nombres instalados se puede mostrar en un símbolo del sistema con el siguiente comando:

**netsh winsock show Catalog**

El kit de desarrollo de software (SDK) de Microsoft Windows incluye *Sporder.exe*, que permite al usuario ver y modificar el orden en el que se enumeran los proveedores de servicios. Con *Sporder.exe*, un usuario puede establecer manualmente una pila de protocolo TCP/IP determinada como el proveedor TCP/IP predeterminado si hay más de una pila de este tipo.

La aplicación *Sporder.exe* utiliza funciones exportadas de *Sporder.dll* para reordenar los proveedores de servicios. Como resultado, las aplicaciones de instalación pueden utilizar la interfaz proporcionada por *Sporder.dll* para reordenar los proveedores de servicios mediante programación.

-   [Protocolos en capas y cadenas de protocolo](layered-protocols-and-protocol-chains-2.md)
-   [Usar varios protocolos](using-multiple-protocols-2.md)
-   [Varias restricciones de proveedor en Select](multiple-provider-restrictions-on-select-2.md)

 

 
