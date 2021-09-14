---
title: Realización de una llamada a procedimiento remoto
description: Una vez que el programa cliente de aplicaciones distribuidas que usa identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Llamada a procedimiento remoto RPC , tareas, realizar una llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a97095d7eda8227f2369f5e3776faf8ce04c22f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244509"
---
# <a name="making-a-remote-procedure-call"></a>Realización de una llamada a procedimiento remoto

Una vez que el programa cliente de aplicaciones distribuidas que usa identificadores de enlace explícitos tiene un identificador de enlace, puede ejecutar procedimientos remotos.

Rpc de Microsoft también ofrece identificadores de enlace personalizados, identificadores de enlace implícitos y identificadores de enlace automático. Estos identificadores de enlace ofrecen programas cliente y servidor diferentes niveles de control sobre el proceso de ejecución de procedimientos remotos. Para obtener más información sobre los distintos tipos de identificadores y la flexibilidad que ofrecen, vea [Enlace y identificadores.](binding-and-handles.md)

Para ejecutar la llamada a procedimiento de forma remota, llame a la función de código auxiliar del lado cliente de la misma manera que se llama a cualquier función de C.

 

 




