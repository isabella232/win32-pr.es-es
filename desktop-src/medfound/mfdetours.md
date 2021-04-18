---
description: Especifica el proveedor de desvío de Microsoft Media Foundation, que realiza un seguimiento de las llamadas a la API Media Foundation.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715368"
---
# <a name="mfdetours-element"></a>elemento mfdetours

Especifica el proveedor de desvío de Microsoft Media Foundation, que realiza un seguimiento de las llamadas a la API Media Foundation.

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
| [**palabra clave**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
keyword+
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                   |
|-------------------------------------------|
| [**providers**](providers.md)<br/> |



## <a name="element-information"></a>Información de elemento



|              |     |
|--------------|-----|
| Puede estar vacío | No  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Archivo de configuración MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




