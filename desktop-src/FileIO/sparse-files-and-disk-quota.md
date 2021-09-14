---
description: Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no a la cantidad real asignada de espacio en disco.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Archivos dispersos y cuotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069839"
---
# <a name="sparse-files-and-disk-quotas"></a>Archivos dispersos y cuotas de disco

Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no a la cantidad real asignada de espacio en disco. Es decir, la creación de un archivo de 50 MB con todos los bytes cero consume 50 MB de la cuota de ese usuario. Esto significa que, a medida que el usuario escribe datos en el archivo disperso, no tiene que preocuparse por superar su límite de cuota fija, ya que ya se le ha cobrado por el espacio. Los administradores del sistema no deben tener en cuenta el tamaño de un archivo disperso que permanece pequeño. Por lo tanto, no deben conceder a sus usuarios límites de cuota fija que superen el espacio físico disponible, a pesar del uso de archivos dispersos.

 

 



