---
description: Especifica el proveedor Microsoft Media Foundation Detours, que hace un seguimiento Media Foundation llamadas API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119340"
---
# <a name="mfdetours-element"></a>elemento mfdetours

Especifica el proveedor Microsoft Media Foundation Detours, que hace un seguimiento Media Foundation llamadas API.

## <a name="usage"></a>Uso

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Atributos



| Atributo            | Tipo             | Obligatorio       | Descripción                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Sí<br/> | Nivel de seguimiento.<br/> <br/> |



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

 

 




