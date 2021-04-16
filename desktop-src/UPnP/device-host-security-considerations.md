---
title: Consideraciones de seguridad del host de dispositivo
description: El uso del host del dispositivo crea problemas de seguridad.
ms.assetid: 7cb445ea-5df4-4030-babd-62527b4d6210
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5a51b90bff33949a33cd9fa1046deb1916ab30
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487863"
---
# <a name="device-host-security-considerations"></a>Consideraciones de seguridad del host de dispositivo

El uso del host de dispositivo crea problemas de seguridad debido a lo siguiente:

-   Los dispositivos alojados en un equipo que ejecuta Windows XP envían anuncios en todas las redes.
-   Los dispositivos hospedados en un equipo que ejecuta Windows XP permiten el control de dispositivos desde todas las redes.

Esto aumenta el riesgo para los consumidores domésticos, ya que los dispositivos como un reproductor de media o una iluminación puente o sistema HVAC hospedados en un equipo que ejecuta Windows XP son visibles y se pueden controlar desde puntos de control fuera de la Página principal.

Al crear un dispositivo hospedado, debe tener en cuenta algunos problemas de seguridad.

-   Para reducir el ámbito de detección y ataque de dispositivos basados en UPnP, el TTL de todos los mensajes SSDP es 1. Esto significa que un dispositivo registrado solo lo detectan los puntos de control de la misma red. Puede configurar un TTL superior en el registro.
-   El registro de un dispositivo que no se está ejecutando requiere el registro previo del archivo Device. dll con COM, lo que requiere privilegios de administrador.
-   El registro de un dispositivo en ejecución requiere privilegios de administrador, servicio local o sistema local.
-   Cuando se inicia el host del dispositivo, se ejecuta como [LocalService](/windows/desktop/Services/localservice-account). Esto proporciona al dispositivo la capacidad de generar auditorías y leer la clave del registro **HKEY \_ local \_ Machine** . El dispositivo tiene acceso a **HKEY \_ Current \_ User**. La cuenta LocalService puede usar los recursos a los que se ha concedido a LocalService, así como los que conceden acceso a AuthenticatedUser. El dispositivo tiene acceso de sistema de archivos restringido.
-   Las ACL del sistema de archivos deben actualizarse para permitir el acceso de [LocalService](/windows/desktop/Services/localservice-account) al directorio de recursos.
-   Si el dispositivo debe tener más acceso de seguridad, puede crear su propio proceso para el dispositivo y registrarlo mediante [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice).

 

 