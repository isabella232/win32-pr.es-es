---
description: Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no por la cantidad de espacio en disco real asignada.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Archivos dispersos y cuotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154604"
---
# <a name="sparse-files-and-disk-quotas"></a>Archivos dispersos y cuotas de disco

Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no por la cantidad de espacio en disco real asignada. Es decir, la creación de un archivo de 50 MB con todos los ceros de bytes consume 50 MB de cuota de usuario. Esto significa que, a medida que el usuario escribe datos en el archivo disperso, no necesita preocuparse por superar su límite de cuota máxima, ya que ya se le ha cargado por el espacio. Los administradores del sistema no deben contar en el tamaño de un archivo disperso que quede pequeño. Por lo tanto, no deben conceder a sus usuarios límites de cuota forzados que superen el espacio físico disponible, a pesar del uso de archivos dispersos.

 

 



