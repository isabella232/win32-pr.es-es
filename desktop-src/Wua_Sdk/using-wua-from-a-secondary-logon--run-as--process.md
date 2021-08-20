---
description: Las actualizaciones que requieren la interacción del usuario no se pueden instalar mediante Windows Update Agent (WUA) si las aplicaciones WUA se ejecutan en el contexto del servicio de inicio de sesión secundario.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a659b9c46429100393138751039fdc1ce529191970a35c76d36e45bb16eb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049093"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Usar WUA desde un proceso de inicio de sesión secundario (ejecutar como)

Las actualizaciones que requieren la interacción del usuario no se pueden instalar mediante Windows Update Agent (WUA) si las aplicaciones WUA se ejecutan en el contexto del servicio de inicio de sesión secundario.

Si el proceso que llama a WUA se ejecuta en el contexto del servicio RunAs o del servicio de inicio de sesión secundario, se produce un error al intentar instalar una actualización que requiere la interacción del usuario y devuelve el error **WU E NO INTERACTIVE \_ \_ \_ \_ USER.**

En Microsoft Windows, puede ejecutar programas como un usuario que difiere del usuario que ha iniciado sesión actualmente. Para ello, el servicio de inicio de sesión secundario debe estar en ejecución.

 

 



