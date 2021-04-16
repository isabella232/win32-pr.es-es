---
description: Las actualizaciones que requieren la interacción del usuario no se pueden instalar con aplicaciones del agente de Windows Update (WUA) si las aplicaciones de WUA se ejecutan en el contexto del servicio de inicio de sesión secundario.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696565"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)

Las actualizaciones que requieren la interacción del usuario no se pueden instalar con aplicaciones del agente de Windows Update (WUA) si las aplicaciones de WUA se ejecutan en el contexto del servicio de inicio de sesión secundario.

Si el proceso que llama a WUA se está ejecutando en el contexto del servicio runas o del servicio de inicio de sesión secundario, se produce un error al intentar instalar una actualización que requiere la interacción del usuario y se devuelve el error de **usuario de Wu \_ E \_ no \_ interactivo \_** .

En Microsoft Windows, puede ejecutar programas como un usuario que difiere del usuario que ha iniciado sesión actualmente. Para ello, el servicio de inicio de sesión secundario debe estar en ejecución.

 

 



