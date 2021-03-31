---
description: Contiene una lista de proveedores de seguimiento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: elemento Providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275822"
---
# <a name="providers-element"></a>elemento Providers

Contiene una lista de proveedores de seguimiento para [MFTrace](mftrace.md).

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
| [**mfdetours**](mfdetours.md)<br/> | Especifica el proveedor de desvío de Media Foundation, que realiza un seguimiento de las llamadas a la API Media Foundation.<br/> <br/> |
| [**presta**](provider.md)<br/>   | Especifica un proveedor de seguimiento (ETW o WPP).<br/> <br/>                                                  |



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



|              |     |
|--------------|-----|
| Puede estar vacío | Sí |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Archivo de configuración MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




