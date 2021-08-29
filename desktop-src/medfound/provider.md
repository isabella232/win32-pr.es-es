---
description: Especifica un proveedor de seguimiento (ETW o WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4213e4d56f8dc2ed73802650e3c7558736cedea8f69fe2148b638fbb92433474
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034973"
---
# <a name="provider-element"></a>provider (elemento)

Especifica un proveedor de seguimiento (ETW o WPP) para [MFTrace.](mftrace.md)

## <a name="usage"></a>Uso

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Atributos



| Atributo            | Tipo             | Requerido       | Descripción                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **Id**<br/>    | CDATA<br/> | Sí<br/> | Nombre o GUID del proveedor.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Sí<br/> | Nivel de seguimiento.<br/> <br/>                  |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                               |
|---------------------------------------|
| [**Palabra clave**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
keyword+
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                   |
|-------------------------------------------|
| [**Proveedores**](providers.md)<br/> |



## <a name="element-information"></a>Información de elemento

:::row:::
    :::column:::
        Puede estar vacío
    :::column-end:::
    :::column span="2":::
        No
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Archivo de configuración de MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




