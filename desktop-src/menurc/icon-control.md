---
title: Control ICON
description: Define un control de icono. Este control es un icono que se muestra en un cuadro de diálogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menús de control ICON y otros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fc5191457996aabe4a70fefcf64235b3a9573cf12733f9ca7bff2ece6356e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034293"
---
# <a name="icon-control"></a>Control ICON

Define un control de icono. Este control es un icono que se muestra en un cuadro de diálogo.

La instrucción de control **ICON,** que solo se puede usar en una instrucción [**DIALOGEX,**](dialogex-resource.md) define el identificador icon-resource, el identificador de control de iconos, la posición y los atributos de un control.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Nombre de un icono (no un nombre de archivo) definido en otra parte del archivo de recursos.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Ancho*
</dt> <dd>

Este valor se omite y debe establecerse en cero.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altura*
</dt> <dd>

Este valor se omite y debe establecerse en cero.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilo de control. Este parámetro es opcional. El único valor que se puede especificar es el **estilo ICON \_ de SS.** Este es el estilo predeterminado tanto si se especifica este parámetro como si no.

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de icono cuyo identificador de icono es 901 y cuyo nombre es myicon:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Icono**](icon-resource.md)
</dt> </dl>

 

 




