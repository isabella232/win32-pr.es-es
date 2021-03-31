---
description: Especifica un proveedor de seguimiento (ETW o WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: provider (elemento)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811575"
---
# <a name="provider-element"></a>provider (elemento)

Especifica un proveedor de seguimiento (ETW o WPP) para [MFTrace](mftrace.md).

## <a name="usage"></a>Uso

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Atributos



| Atributo            | Tipo             | Obligatorio       | Descripción                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **Id**<br/>    | CDATA<br/> | Sí<br/> | El nombre o GUID del proveedor.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Sí<br/> | Nivel de seguimiento.<br/> <br/>                  |



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

 

 




