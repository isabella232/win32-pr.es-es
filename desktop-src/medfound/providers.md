---
description: Contiene una lista de proveedores de seguimiento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268764"
---
# <a name="providers-element"></a>Elemento providers

Contiene una lista de proveedores de seguimiento [para MFTrace.](mftrace.md)

## <a name="usage"></a>Uso

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> | Especifica el proveedor Media Foundation Detours, que hace un seguimiento Media Foundation llamadas API.<br/> <br/> |
| [**Proveedor**](provider.md)<br/>   | Especifica un proveedor de seguimiento (ETW o WPP).<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>Elementos primarios

No hay elementos primarios.

## <a name="element-information"></a>Información de elemento

:::row:::
    :::column:::
        Puede estar vacío
    :::column-end:::
    :::column span="2":::
        Sí
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Archivo de configuración de MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




