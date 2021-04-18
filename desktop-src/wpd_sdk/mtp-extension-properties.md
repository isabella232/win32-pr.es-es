---
description: Propiedades de extensión MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propiedades de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720580"
---
# <a name="mtp-extension-properties"></a>Propiedades de extensión MTP

Las propiedades describen objetos, propiedades, recursos y dispositivos.

## <a name="vendor-extended-object-properties"></a>Propiedades de objetos extendidos de proveedor

Cuando un fabricante de dispositivos crea una propiedad de proveedor extendida para un objeto de dispositivo, combina el GUID de **\_ propiedades de \_ \_ \_ objetos extendidos del proveedor \_ \_ MTP** de las propiedades de WPD con el código de propiedad del objeto para construir una estructura **PROPERTYKEY** .

Por ejemplo, si el código de propiedad del objeto es 0xD801, el **PROPERTYKEY** resultante sería como se muestra en el ejemplo siguiente:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Propiedades de dispositivo extendido de proveedor

Cuando un fabricante de dispositivos crea una propiedad de proveedor extendida para un dispositivo, combina el GUID de **\_ propiedades de \_ \_ \_ \_ dispositivo \_ extendido del proveedor MTP** de las propiedades de WPD con el código de propiedad del objeto para crear una estructura **PROPERTYKEY** .

Por ejemplo, si el código de propiedad del objeto es 0xD001, el **PROPERTYKEY** resultante sería como se muestra en el ejemplo siguiente:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



