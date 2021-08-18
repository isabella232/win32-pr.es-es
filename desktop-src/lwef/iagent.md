---
title: IAgent
description: IAgent
ms.assetid: 35b12006-a938-450c-969a-7b73a3768a4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3931c277fbe4a5943ef5881da12cf3669b2e8894c95052f61bc8411e21c7ae3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751438"
---
# <a name="iagent"></a>IAgent

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

**IAgent** define una interfaz que permite a las aplicaciones cargar caracteres, recibir eventos y comprobar el estado actual de Microsoft Agent Server. Estas funciones también están disponibles en [**IAgentEx.**](iagentex.md)

El método GetSuspended incluido en versiones anteriores está obsoleto y devuelve **False** por compatibilidad con versiones anteriores.

**Métodos en orden de Vtable**



| Métodos IAgent                               | Descripción                                                   |
|----------------------------------------------|---------------------------------------------------------------|
| [**Cargar**](load-method.md)                  | Carga el archivo de datos de un carácter.                                |
| [**Descargar**](unload-method.md)              | Descarga el archivo de datos de un carácter.                              |
| [**Registro**](iagent--register.md)         | Registra un receptor de notificaciones para el cliente.                 |
| [**Unegister**](iagent--unregister.md)      | Anula el registro del receptor de notificaciones de un cliente.                     |
| [**GetCharacter**](iagent--getcharacter.md) | Devuelve la interfaz IAgentCharacter para un carácter cargado. |



 

 

 




