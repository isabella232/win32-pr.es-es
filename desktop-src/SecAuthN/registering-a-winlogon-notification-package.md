---
description: La información sobre los paquetes de notificación de Winlogon se almacena en el registro. Las entradas del Registro especifican el nombre del paquete de notificación, el nombre del archivo DLL que implementa el paquete y los nombres de las funciones que controlan eventos winlogon.
ms.assetid: dbe8d5a3-8927-4b95-a1a0-82c8e12ba8c1
title: Registro de un paquete de notificación de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25b353220727c828a0fa0b1d6f9b479bfa54832e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069129"
---
# <a name="registering-a-winlogon-notification-package"></a>Registro de un paquete de notificación de Winlogon

La información sobre los paquetes de notificación de [*Winlogon*](../secgloss/w-gly.md) se almacena en el registro. Las entradas del Registro especifican el nombre del paquete de notificación, el nombre del archivo DLL que implementa el paquete y los nombres de las funciones que controlan eventos winlogon.

Cuando se inicia Winlogon, comprueba el registro y carga los paquetes de notificación registrados. Cuando se produce un evento, Winlogon llama a la función de controlador de eventos designada para cada paquete. Se pueden registrar varios paquetes de notificación de eventos en un sistema.

Para registrar el paquete de notificación, cree una clave del Registro denominada **Notify** como subclave de la siguiente clave del Registro y agregue los valores detallados en [Entradas del Registro](registry-entries.md).

**HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon**

 

 
