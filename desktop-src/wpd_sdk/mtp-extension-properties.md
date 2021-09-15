---
description: Propiedades de la extensión MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propiedades de la extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572104"
---
# <a name="mtp-extension-properties"></a>Propiedades de la extensión MTP

Las propiedades describen objetos, propiedades, recursos y dispositivos.

## <a name="vendor-extended-object-properties"></a>Propiedades de objetos extendidos por el proveedor

Cuando un fabricante de dispositivos crea una propiedad extendida por el proveedor para un objeto de dispositivo, combina el GUID DE PROPS DE OBJETOS **\_ \_ \_ \_ \_ \_ EXTENDIDOS MTP PROPERTIES MTP PROPERTIES** con el código de propiedad del objeto para construir una **estructura PROPERTYKEY.**

Por ejemplo, si el código de propiedad del objeto es 0xD801, **propertyKEY** resultante sería como se muestra en el ejemplo siguiente:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Propiedades de dispositivo extendidas por el proveedor

Cuando un fabricante de dispositivos crea una propiedad extendida por el proveedor para un dispositivo, combina el GUID de **\_ \_ \_ \_ \_ \_ PROPS** DE DISPOSITIVO EXTENDIDO MTP PROPERTIES MTP PROPERTIES con el código de propiedad del objeto para construir una **estructura PROPERTYKEY.**

Por ejemplo, si el código de propiedad del objeto es 0xD001, **propertyKEY** resultante sería como se muestra en el ejemplo siguiente:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones de MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



