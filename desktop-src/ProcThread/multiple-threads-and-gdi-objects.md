---
description: Para mejorar el rendimiento, el acceso a los objetos de la interfaz de dispositivo gráfico (GDI) (como las paletas, los contextos de dispositivo, las regiones y el like) no se serializan.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Varios subprocesos y objetos GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677856"
---
# <a name="multiple-threads-and-gdi-objects"></a>Varios subprocesos y objetos GDI

Para mejorar el rendimiento, el acceso a los objetos de la interfaz de dispositivo gráfico (GDI) (como las paletas, los contextos de dispositivo, las regiones y el like) no se serializan. Esto crea un riesgo potencial para los procesos que tienen varios subprocesos que comparten estos objetos. Por ejemplo, si un subproceso elimina un objeto GDI mientras otro subproceso lo está usando, los resultados son imprevisibles. Este peligro se puede evitar simplemente si no se comparten objetos GDI. Si el uso compartido es inevitable (o deseable), la aplicación debe proporcionar sus propios mecanismos para sincronizar el acceso. Para obtener más información sobre cómo sincronizar el acceso, vea [sincronizar la ejecución de varios subprocesos](synchronizing-execution-of-multiple-threads.md).

 

 



