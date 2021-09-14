---
title: Caché de atributos ADSI
description: El modelo de objetos ADSI proporciona una caché de atributos del lado cliente para cada objeto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- The ADSI Attribute Cache ADSI
- ADSI ADSI, uso, acceso y manipulación de datos con ADSI, caché de atributos
- atributos ADSI, almacenamiento en caché de atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172109"
---
# <a name="the-adsi-attribute-cache"></a>Caché de atributos ADSI

El modelo de objetos ADSI proporciona una caché de atributos del lado cliente para cada objeto ADSI. La caché de atributos es comparable a una tabla en memoria que contiene los nombres y valores de la mayoría de los atributos de objeto que se han descargado. Algunos atributos, como los atributos operativos, no se almacenan en caché. ADSI usa el almacenamiento en caché de propiedades para mejorar el rendimiento de la manipulación de atributos y agregar funcionalidad de transacción para las operaciones de lectura y escritura de atributos. Esta funcionalidad es fundamental para los clientes escritos en lenguajes que no tienen ningún mecanismo de procesamiento por lotes nativo para establecer atributos, como Microsoft Visual Basic de desarrollo. Sin la caché de propiedades adsi, estos clientes tendrían que acceder al servidor cada vez que se lee o escribe un atributo.

Cuando se crea un objeto o se enlaza primero a él, la caché de propiedades del objeto está vacía. Cuando se [**llama al método IADs::GetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ADSI carga los atributos solicitados para el objeto desde el servicio de directorio subyacente en la memoria caché local. Cuando se lee un valor de atributo específico y la memoria caché está vacía, ADSI realiza una llamada implícita al método **IADs::GetInfo.** Cuando se rellena la memoria caché, todas las operaciones de lectura de atributos solo funcionan en el contenido de la memoria caché.

Cuando se escribe un valor de atributo, el nuevo valor se almacena en la memoria caché local hasta que se llama al método [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Cuando se **llama al método IADs::SetInfo,** los atributos de la memoria caché se confirman en el servicio de directorio subyacente. Después de llamar al método **IADs::SetInfo,** los valores permanecen en la memoria caché hasta que se actualicen explícitamente con otra llamada al método [**IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)

> [!IMPORTANT]
> El [**método IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) debe usarse cuidadosamente porque este método siempre sobrescribirá los valores de atributo de la memoria caché desde el servicio de directorio subyacente, incluso si se ha cambiado el valor almacenado en caché. Es decir, sobrescribirá los valores de atributo que se han cambiado en la memoria caché, pero no se confirman en el servicio de directorio subyacente con una llamada al método [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

 

En la ilustración siguiente se muestran los distintos métodos usados para operar en la memoria caché.

![Caché de atributos adsi](images/ds2propc.png)

 

 




