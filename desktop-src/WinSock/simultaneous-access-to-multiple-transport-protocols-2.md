---
description: Un protocolo de transporte debe estar correctamente instalado en el sistema y registrado con Windows sockets para que una aplicación pueda acceder a él.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Acceso simultáneo a varios protocolos de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9648a7ffe1c4c0b1627ea46cd2956b48ba574adb468d750a2c4095a32783746f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118111552"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a>Acceso simultáneo a varios protocolos de transporte

Un protocolo de transporte debe estar correctamente instalado en el sistema y registrado con Windows sockets para que una aplicación pueda acceder a él. La biblioteca de \_32.dll Ws2 exporta un conjunto de funciones para facilitar el proceso de registro. Esto incluye la creación de un nuevo registro y la eliminación de uno existente.

Cuando se crean nuevos registros, el autor de la llamada (es decir, el script de instalación del proveedor de la pila) proporciona una o varias estructuras info de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) rellenas que contienen un conjunto completo de información sobre el protocolo. Para obtener más información, [vea Windows Sockets 2 SPI](about-the-winsock-spi.md). Cualquier pila de transporte instalada de esta manera se conoce como proveedor de servicios Windows Sockets.

En Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) y Windows Vista y versiones posteriores. El catálogo de Winsock que contiene una lista de proveedores de transporte y espacio de nombres instalados se puede mostrar en un símbolo del sistema con el siguiente comando:

**netsh winsock show catalog**

Microsoft Windows Software Development Kit (SDK) incluye *Sporder.exe*, que permite al usuario ver y modificar el orden en que se enumeran los proveedores de servicios. Con *Sporder.exe*, un usuario puede establecer manualmente una pila de protocolo TCP/IP determinada como proveedor tcp/IP predeterminado si hay más de una pila de este tipo.

La *Sporder.exe* utiliza funciones exportadas de *Sporder.dll* para reordenar los proveedores de servicios. Como resultado, las aplicaciones de instalación pueden usar la interfaz proporcionada por *Sporder.dll* para reordenar los proveedores de servicios mediante programación.

-   [Protocolos por capas y cadenas de protocolo](layered-protocols-and-protocol-chains-2.md)
-   [Uso de varios protocolos](using-multiple-protocols-2.md)
-   [Restricciones de varios proveedores al seleccionar](multiple-provider-restrictions-on-select-2.md)

 

 
