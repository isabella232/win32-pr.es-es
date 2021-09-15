---
title: Inicio y detención del localizador de Microsoft
description: Las bibliotecas rpc en tiempo de ejecución inician automáticamente Microsoft Locator cuando es necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, necesita borrar la base de datos al depurar una aplicación distribuida.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473505"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Inicio y detención del localizador de Microsoft

Las bibliotecas rpc en tiempo de ejecución inician automáticamente Microsoft Locator cuando es necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, necesita borrar la base de datos al depurar una aplicación distribuida.

**Para detener e iniciar Microsoft Locator**

1.  En Panel de control, haga clic en el icono Servicios.

    Aparece **el cuadro** de diálogo Servicios.

2.  En el cuadro **de diálogo** Servicio, seleccione Localizador **de Microsoft** y, a continuación, haga clic en **Iniciar** **o Detener.**

También puede iniciar y detener Microsoft Locator desde la línea de comandos escribiendo:

**net \[ start/stop \] rpclocator**

Solo un administrador puede iniciar Microsoft Locator una vez detenido. Si se detiene, las bibliotecas en tiempo de ejecución de RPC lo reiniciarán según sea necesario.

 

 




