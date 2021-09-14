---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12900a4288b9917d695dd25d4b81362b67c93587
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127269492"
---
# <a name="iagent"></a>IAgent

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

**IAgent** define una interfaz que permite a las aplicaciones cargar caracteres, recibir eventos y comprobar el estado actual de Microsoft Agent Server. Estas funciones también están disponibles en [**IAgentEx.**](iagentex.md)

El método GetSuspended incluido en versiones anteriores está obsoleto y devuelve **False** por compatibilidad con versiones anteriores.

**Métodos en orden de Vtable**



| Métodos IAgent                               | Descripción                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Carga**](load-method.md)                  | Carga el archivo de datos de un carácter.                                |
| [**Descargar**](unload-method.md)              | Descarga el archivo de datos de un carácter.                              |
| [**Registrarse**](iagent--register.md)         | Registra un receptor de notificaciones para el cliente.                 |
| [**Unegister**](iagent--unregister.md)      | Anula el registro del receptor de notificaciones de un cliente.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Devuelve la interfaz IAgentCharacter para un carácter cargado. |



 

 

 




