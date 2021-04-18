---
description: Especifica una palabra clave para un proveedor MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707015"
---
# <a name="keyword-element"></a>elemento keyword

Especifica una palabra clave para un proveedor [MFTrace](mftrace.md) .

## <a name="usage"></a>Uso

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Atributos



| Atributo         | Tipo             | Obligatorio       | Descripción                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **Id**<br/> | CDATA<br/> | Sí<br/> | El nombre o la máscara de la palabra clave<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**presta**](provider.md)<br/>   |



## <a name="remarks"></a>Observaciones

En el caso del elemento [**mfdetours**](mfdetours.md) , se enumeran las palabras clave válidas en el tema palabras clave de [MFTrace](mftrace-keywords.md).

En el caso del elemento [**Provider**](provider.md) , las palabras clave dependen del proveedor de eventos. Puede usar la utilidad Wevtutil.exe para mostrar las palabras clave de un proveedor determinado.

## <a name="element-information"></a>Información de elemento



|              |     |
|--------------|-----|
| Puede estar vacío | Sí |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Archivo de configuración MFTrace](mftrace-configuration-file.md)
</dt> <dt>

[Palabras clave de MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 




