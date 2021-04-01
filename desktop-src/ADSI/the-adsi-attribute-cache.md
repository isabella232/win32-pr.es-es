---
title: La caché de atributos ADSI
description: El modelo de objetos ADSI proporciona una caché de atributos de cliente para cada objeto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- La caché de atributos ADSI ADSI
- ADSI ADSI, uso, acceso y manipulación de datos con ADSI, caché de atributos
- atributos ADSI, almacenamiento en caché de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772912"
---
# <a name="the-adsi-attribute-cache"></a>La caché de atributos ADSI

El modelo de objetos ADSI proporciona una caché de atributos de cliente para cada objeto ADSI. La caché de atributos es comparable a una tabla en memoria que contiene los nombres y los valores de la mayoría de los atributos de objeto que se han descargado. Algunos atributos, como los atributos operativos, no se almacenan en caché. ADSI usa el almacenamiento en caché de propiedades para mejorar el rendimiento de la manipulación de atributos y agregar la capacidad de transacción para las operaciones de lectura y escritura de atributos. Esta funcionalidad es fundamental para los clientes escritos en lenguajes que no tienen ningún mecanismo de procesamiento por lotes nativo para establecer atributos, como el sistema de desarrollo de Microsoft Visual Basic. Sin la memoria caché de propiedades ADSI, estos clientes tendrían que acceder al servidor cada vez que se lee o escribe un atributo.

Cuando se crea un objeto o se enlaza primero a, la memoria caché de propiedades del objeto está vacía. Cuando se llama al método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) , ADSI carga los atributos solicitados para el objeto desde el servicio de directorio subyacente en la caché local. Cuando se lee un valor de atributo concreto y la memoria caché está vacía, ADSI realiza una llamada implícita al método **IADs:: GetInfo** . Cuando se rellena la memoria caché, todas las operaciones de lectura de atributo solo funcionan en el contenido de la memoria caché.

Cuando se escribe un valor de atributo, el nuevo valor se almacena en la memoria caché local hasta que se llama al método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Cuando se llama al método **IADs:: SetInfo** , los atributos de la memoria caché se confirman en el servicio de directorio subyacente. Después de llamar al método **IADs:: SetInfo** , los valores permanecen en la memoria caché hasta que se actualizan explícitamente con otra llamada al método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .

> [!IMPORTANT]
> El método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) debe utilizarse con cuidado, ya que este método siempre sobrescribirá los valores de atributo en la memoria caché del servicio de directorio subyacente, incluso si se ha cambiado el valor almacenado en caché. Es decir, sobrescribirá los valores de atributo que se han modificado en la memoria caché, pero que no se han confirmado en el servicio de directorio subyacente con una llamada al método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

 

En la siguiente ilustración se muestran los distintos métodos que se usan para operar en la memoria caché.

![caché de atributos ADSI](images/ds2propc.png)

 

 




