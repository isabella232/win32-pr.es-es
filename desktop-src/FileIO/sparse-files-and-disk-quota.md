---
description: Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no la cantidad real asignada de espacio en disco.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Archivos dispersos y cuotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e78e9d35e557585f17df6c4672a04b2997792f95b0fca63d2e6a2345a7a8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015083"
---
# <a name="sparse-files-and-disk-quotas"></a>Archivos dispersos y cuotas de disco

Un archivo disperso afecta a las cuotas de usuario por el tamaño nominal del archivo, no la cantidad real asignada de espacio en disco. Es decir, la creación de un archivo de 50 MB con cero bytes consume 50 MB de la cuota de ese usuario. Esto significa que, a medida que el usuario escribe datos en el archivo disperso, no tiene que preocuparse por superar su límite de cuota fija, ya que ya se le ha cobrado por el espacio. Los administradores del sistema no deben contar con el tamaño de un archivo disperso que sigue siendo pequeño. Por lo tanto, no deben conceder a sus usuarios límites de cuota de duración que superen el espacio físico disponible, a pesar del uso de archivos dispersos.

 

 



