---
description: La noción de bloqueo en un entorno Windows ha sido históricamente muy importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operaciones de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322440"
---
# <a name="blocking-operations"></a>Operaciones de bloqueo

La noción de bloqueo en un entorno Windows ha sido históricamente muy importante. En Windows sockets 1.1, se desaconsejaban las llamadas de bloqueo, ya que tendían a deshabilitar la interacción continua con el sistema. Además, emplean una técnica de pseudobloqueo que, por diversos motivos, no siempre funciona según lo previsto. Sin embargo, en entornos de Windows programados de forma preferente, las llamadas de bloqueo tienen mucho más sentido, pueden implementarse mediante servicios de sistema operativo nativos y, de hecho, son un mecanismo preferido por lo general. La API winsock 2 ya no admite psuedoblocking, pero dado que las correcciones de compatibilidad de Windows Sockets 1.1 deben seguir emulando este comportamiento, los proveedores de servicios deben admitirlo como se describe a continuación.

 

 



