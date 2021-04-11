---
description: La información acerca de los paquetes de notificación Winlogon se almacena en el registro. Las entradas del registro especifican el nombre del paquete de notificación, el nombre del archivo DLL que implementa el paquete y los nombres de las funciones que controlan los eventos de Winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registrar un paquete de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276686"
---
# <a name="registering-a-winlogon-notification-package"></a>Registrar un paquete de notificación de Winlogon

La información acerca de los paquetes de notificación [*Winlogon*](../secgloss/w-gly.md) se almacena en el registro. Las entradas del registro especifican el nombre del paquete de notificación, el nombre del archivo DLL que implementa el paquete y los nombres de las funciones que controlan los eventos de Winlogon.

Cuando se inicia Winlogon, comprueba el registro y carga los paquetes de notificación registrados. Cuando se produce un evento, Winlogon llama a la función de controlador de eventos designada para cada paquete. Se pueden registrar varios paquetes de notificación de eventos en un sistema.

Para registrar el paquete de notificación, cree una clave del registro denominada **Notify** como subclave de la siguiente clave del registro y agregue los valores detallados en [las entradas del registro](registry-entries.md).

**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
