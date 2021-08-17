---
description: Propiedades de la extensión MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propiedades de la extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0468d249b469c4e768962ab6a920935e7a64b51d8e035af111e8274f7f0b9af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193951"
---
# <a name="mtp-extension-properties"></a>Propiedades de la extensión MTP

Las propiedades describen objetos, propiedades, recursos y dispositivos.

## <a name="vendor-extended-object-properties"></a>Propiedades de objetos extendidos del proveedor

Cuando un fabricante de dispositivos crea una propiedad extendida por el proveedor para un objeto de dispositivo, combina el GUID de PROPS DE OBJETOS **\_ \_ \_ \_ \_ \_ EXTENDIDOS MTP PROPERTIES MTP PROPERTIES** con el código de propiedad del objeto para construir una **estructura PROPERTYKEY.**

Por ejemplo, si el código de propiedad del objeto es 0xD801, el **VALOR PROPERTYKEY** resultante sería como se muestra en el ejemplo siguiente:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Propiedades de dispositivo extendidas por el proveedor

Cuando un fabricante de dispositivos crea una propiedad extendida por el proveedor para un dispositivo, combina el GUID de **\_ \_ \_ \_ \_ \_ PROPS** DE DISPOSITIVO EXTENDIDO DE MTP PROPERTIES MTP PROPERTIES con el código de propiedad del objeto para construir una **estructura PROPERTYKEY.**

Por ejemplo, si el código de propiedad del objeto 0xD001, el **propertyKEY** resultante sería como se muestra en el ejemplo siguiente:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



