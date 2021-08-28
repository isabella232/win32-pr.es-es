---
title: Inicio y detención del localizador de Microsoft
description: Las bibliotecas rpc en tiempo de ejecución inician automáticamente Microsoft Locator cuando es necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, necesita borrar la base de datos durante la depuración de una aplicación distribuida.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e281419bc2a869d43863f946c1fcb172da2f86c04186ba775766233d4caa65c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017555"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Inicio y detención del localizador de Microsoft

Las bibliotecas rpc en tiempo de ejecución inician automáticamente Microsoft Locator cuando es necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, necesita borrar la base de datos durante la depuración de una aplicación distribuida.

**Para detener e iniciar Microsoft Locator**

1.  En Panel de control, haga clic en el icono Servicios.

    Aparece **el cuadro** de diálogo Servicios.

2.  En el cuadro **de diálogo** Servicio, seleccione Localizador **de Microsoft** y, a continuación, haga clic en **Iniciar** **o Detener.**

También puede iniciar y detener Microsoft Locator desde la línea de comandos escribiendo:

**net \[ start/stop \] rpclocator**

Solo un administrador puede iniciar Microsoft Locator una vez detenido. Si se detiene, las bibliotecas en tiempo de ejecución de RPC lo reiniciarán según sea necesario.

 

 




