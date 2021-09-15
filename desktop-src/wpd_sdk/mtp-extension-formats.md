---
description: Formatos de extensión MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formatos de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572105"
---
# <a name="mtp-extension-formats"></a>Formatos de extensión MTP

El formato de un archivo en un dispositivo se puede describir mediante un valor GUID. La propiedad WPD OBJECT FORMAT especifica \_ \_ este valor.

## <a name="vendor-extended-formats"></a>Formatos extendidos del proveedor

Cuando un fabricante de dispositivos admite un formato extendido por el proveedor, su controlador combina el código de formato del proveedor (UINT16) con los 16 bits más altos del GUID **WPD \_ OBJECT FORMAT \_ \_ UNSPECIFIED.**

Por ejemplo, si el código extendido del proveedor 0xB001, el GUID resultante sería como se muestra en el ejemplo siguiente:


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compatibilidad con extensiones MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 



