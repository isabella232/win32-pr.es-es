---
description: Para mejorar el rendimiento, no se serializa el acceso a objetos de interfaz de dispositivo gráfico (GDI) (como paletas, contextos de dispositivo, regiones y otros).
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Varios subprocesos y objetos GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375034"
---
# <a name="multiple-threads-and-gdi-objects"></a>Varios subprocesos y objetos GDI

Para mejorar el rendimiento, no se serializa el acceso a objetos de interfaz de dispositivo gráfico (GDI) (como paletas, contextos de dispositivo, regiones y otros). Esto crea un riesgo potencial para los procesos que tienen varios subprocesos que comparten estos objetos. Por ejemplo, si un subproceso elimina un objeto GDI mientras otro subproceso lo usa, los resultados son impredecibles. Este peligro se puede evitar simplemente si no se comparten objetos GDI. Si el uso compartido es inevitable (o deseable), la aplicación debe proporcionar sus propios mecanismos para sincronizar el acceso. Para obtener más información sobre cómo sincronizar el acceso, vea Sincronizar la ejecución [de varios subprocesos.](synchronizing-execution-of-multiple-threads.md)

 

 



