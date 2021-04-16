---
description: La noción de bloqueo en un entorno de Windows ha sido históricamente muy importante.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Operaciones de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696404"
---
# <a name="blocking-operations"></a>Operaciones de bloqueo

La noción de bloqueo en un entorno de Windows ha sido históricamente muy importante. En entornos Windows Sockets 1,1, no se recomiendan las llamadas de bloqueo, ya que solían deshabilitar la interacción continua con el sistema. Además, emplean una técnica pseudoblocking que, por diversos motivos, no siempre funciona según lo previsto. Sin embargo, en entornos de Windows programados de forma preventiva, las llamadas de bloqueo tienen mucho más sentido, pueden ser implementadas por los servicios del sistema operativo nativo y, en realidad, son un mecanismo preferido. La API de Winsock 2 ya no es compatible con psuedoblocking, pero debido a que las correcciones de compatibilidad de Windows Sockets 1,1 deben seguir emulando este comportamiento, los proveedores de servicios deben admitir esto tal y como se describe a continuación.

 

 



