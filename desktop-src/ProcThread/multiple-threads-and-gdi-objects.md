---
description: Para mejorar el rendimiento, no se serializa el acceso a objetos de interfaz de dispositivo gráfico (GDI) (como paletas, contextos de dispositivo, regiones, entre otros).
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Varios subprocesos y objetos GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a17c7edcf32341eb9b1eaff3546fbe7be219b5f924a85d4a1db1d584a0a5922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032335"
---
# <a name="multiple-threads-and-gdi-objects"></a>Varios subprocesos y objetos GDI

Para mejorar el rendimiento, no se serializa el acceso a objetos de interfaz de dispositivo gráfico (GDI) (como paletas, contextos de dispositivo, regiones, entre otros). Esto crea un riesgo potencial para los procesos que tienen varios subprocesos que comparten estos objetos. Por ejemplo, si un subproceso elimina un objeto GDI mientras otro subproceso lo usa, los resultados son impredecibles. Este peligro se puede evitar simplemente al no compartir objetos GDI. Si el uso compartido es inevitable (o deseable), la aplicación debe proporcionar sus propios mecanismos para sincronizar el acceso. Para obtener más información sobre cómo sincronizar el acceso, vea [Sincronizar la ejecución de varios subprocesos.](synchronizing-execution-of-multiple-threads.md)

 

 



