---
description: Si un subproceso está esperando a que se complete una devolución de llamada en modo kernel, el lado del modo de usuario del subproceso se retrasará en una llamada a la función ZwCallbackReturn.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Detección de Kernel-Mode devoluciones de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029ecf7d5b1f9220de51c2ecffe4bdf30da4cbd088d9d251fd0d24bab04934e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691455"
---
# <a name="detecting-kernel-mode-callbacks"></a>Detección de Kernel-Mode devoluciones de llamada

La mayor parte del código para el sistema Windows operativo se ejecuta en modo kernel. El modo de procesador cambia del modo de usuario al modo kernel cada vez que un subproceso de aplicación llama a una función de la API de Windows que, a su vez, llama a una función interna del sistema que debe ejecutarse en modo kernel. El modo de procesador vuelve al modo de usuario antes de que el control vuelva a la función para que los datos del sistema estén protegidos.

Si un subproceso está esperando a que se complete una devolución de llamada en modo kernel, el lado del modo de usuario del subproceso se retrasará en una llamada a la **función ZwCallbackReturn.**

 

 



