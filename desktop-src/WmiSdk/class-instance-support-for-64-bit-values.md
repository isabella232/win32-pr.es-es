---
description: Proporciona restricciones para el uso de valores de 64 bits como parte de una ruta de acceso.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Compatibilidad de instancia de clase con valores de 64 bits
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 80f8a48f253cf2ef1902938ca6c54d01404b8466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678165"
---
# <a name="class-instance-support-for-64-bit-values"></a>Compatibilidad de instancia de clase con valores de 64 bits

Puede usar un valor de clave de 64 bits como parte de una ruta de acceso, con las restricciones siguientes:

-   Siempre que no supere el intervalo de 32 bits, puede asignar y recuperar valores de la clave como lo haría con una propiedad de 32 bits.
-   Una vez superado el valor entero de 0x7FFFFFFF (para tipos con signo), 0x80000000 (para tipos sin signo) o 32 bits, debe usar comillas.
-   La única ruta de acceso válida para un valor de 64 bits se encuentra en las propiedades **\_ \_ RELPATH** o **\_ \_ path** de la instancia. Como tal, WMI no admite la notación hexadecimal para el valor equivalente.
-   Si WMI registra la clave de instancia como un número negativo, debe utilizar el número original para recuperar la instancia.

La semántica de consulta no se ve afectada y se comporta según lo esperado. Este comportamiento solo afecta a las operaciones de ruta de acceso de objeto, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)y [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

En el ejemplo siguiente se muestra que las instancias de clase pueden tener valores de clave de 64 bits.

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



