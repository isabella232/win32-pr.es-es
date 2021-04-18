---
description: Formatos de extensión MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formatos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720581"
---
# <a name="mtp-extension-formats"></a>Formatos de extensión MTP

El formato de un archivo en un dispositivo se puede describir mediante un valor GUID. Este valor se especifica mediante la \_ propiedad formato de objeto WPD \_ .

## <a name="vendor-extended-formats"></a>Formatos extendidos de proveedor

Cuando un fabricante de dispositivos admite un formato extendido de proveedor, el controlador combina el código de formato del proveedor (UINT16) con los 16 bits superiores **del \_ formato de objeto WPD sin \_ \_ especificar** .

Por ejemplo, si el código extendido del proveedor es 0xB001, el GUID resultante sería como se muestra en el ejemplo siguiente:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



