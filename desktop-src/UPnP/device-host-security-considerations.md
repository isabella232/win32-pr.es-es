---
title: Consideraciones de seguridad del host de dispositivos
description: El uso del host de dispositivo crea problemas de seguridad.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4e8cdce90cdc5801010833db4cb97c49487c16a3926bf235f126f33e1078f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008095"
---
# <a name="device-host-security-considerations"></a>Consideraciones de seguridad del host de dispositivos

El uso del host de dispositivo crea problemas de seguridad debido a lo siguiente:

-   Los dispositivos hospedados en un equipo Windows XP envían anuncios en todas las redes.
-   Los dispositivos hospedados en un equipo que Windows XP permiten el control de dispositivos de todas las redes.

Esto aumenta el riesgo para los consumidores del hogar, ya que los dispositivos como un reproductor multimedia, una iluminación puente o un sistema HVAC hospedado en un equipo que ejecuta Windows XP son visibles y se pueden controlar desde puntos de control fuera del hogar.

Al crear un dispositivo hospedado, debe tener en cuenta algunos problemas de seguridad.

-   Para reducir el ámbito de detección y ataque de los dispositivos basados en UPnP, el TTL de todos los mensajes SSDP es 1. Esto significa que los puntos de control de la misma red solo detectan un dispositivo registrado. Puede configurar un TTL superior en el Registro.
-   El registro de un dispositivo que no se ejecuta requiere el registro previo del dispositivo .dll con COM, lo que requiere privilegios de administrador.
-   El registro de un dispositivo en ejecución requiere privilegios de administrador, servicio local o sistema local.
-   Cuando se inicia el host de dispositivo, se ejecuta como [LocalService](/windows/desktop/Services/localservice-account). Esto proporciona al dispositivo la capacidad de generar auditorías y leer la clave del Registro **HKEY \_ LOCAL \_ MACHINE.** El dispositivo tiene acceso a **HKEY \_ CURRENT \_ USER**. La cuenta LocalService puede usar recursos a los que se ha concedido acceso a LocalService, así como aquellos que conceden acceso a AuthenticatedUser. El dispositivo tiene acceso restringido al sistema de archivos.
-   Las ACL del sistema de archivos deben actualizarse para permitir el [acceso de LocalService](/windows/desktop/Services/localservice-account) al directorio de recursos.
-   Si el dispositivo debe tener más acceso de seguridad, puede crear su propio proceso para el dispositivo y registrarlo mediante [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 