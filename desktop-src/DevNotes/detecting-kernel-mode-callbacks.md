---
description: Si un subproceso está esperando a que se complete una devolución de llamada de modo kernel, el lado del modo de usuario del subproceso retrasará en una llamada a la función ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Detección de devoluciones de llamada de Kernel-Mode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000708"
---
# <a name="detecting-kernel-mode-callbacks"></a>Detección de devoluciones de llamada de Kernel-Mode

La mayor parte del código para el sistema operativo Windows se ejecuta en modo kernel. El modo de procesador cambia del modo de usuario al modo kernel siempre que un subproceso de aplicación llama a una función de la API de Windows que, a su vez, llama a una función del sistema interna que debe ejecutarse en modo kernel. El modo de procesador vuelve al modo de usuario antes de que el control vuelva a la función de modo que los datos del sistema estén protegidos.

Si un subproceso está esperando a que se complete una devolución de llamada de modo kernel, el lado del modo de usuario del subproceso retrasará en una llamada a la función **ZwCallbackReturn** .

 

 



