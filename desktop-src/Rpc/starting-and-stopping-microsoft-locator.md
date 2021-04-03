---
title: Iniciar y detener el localizador de Microsoft
description: Las bibliotecas en tiempo de ejecución de RPC inician automáticamente el localizador de Microsoft cuando sea necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, tiene que borrar la base de datos durante la depuración de una aplicación distribuida.
ms.assetid: 06b50a9f-b640-45b2-86e2-2bcea6c16c5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433ffdb11e86b06ee53d9b01f7f7755758538f22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075007"
---
# <a name="starting-and-stopping-microsoft-locator"></a>Iniciar y detener el localizador de Microsoft

Las bibliotecas en tiempo de ejecución de RPC inician automáticamente el localizador de Microsoft cuando sea necesario. Puede detener e iniciar manualmente el localizador si, por ejemplo, tiene que borrar la base de datos durante la depuración de una aplicación distribuida.

**Para detener e iniciar el localizador de Microsoft**

1.  En el panel de control, haga clic en el icono servicios.

    Aparece el cuadro de diálogo **servicios** .

2.  En el cuadro de diálogo **servicio** , seleccione **localizador de Microsoft** y, a continuación, haga clic en **iniciar** o **detener**.

También puede iniciar y detener el localizador de Microsoft desde la línea de comandos escribiendo lo siguiente:

**NET \[ Start/Stop \] rpclocator**

Solo un administrador puede iniciar el localizador de Microsoft una vez detenido. Si se detiene, se reiniciará según las necesidades de las bibliotecas en tiempo de ejecución de RPC.

 

 




