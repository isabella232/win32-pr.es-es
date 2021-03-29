---
title: Control de icono
description: Define un control de icono. Este control es un icono que se muestra en un cuadro de diálogo.
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- Menús de control de icono y otros recursos
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2400136395a17f039d552373fa35cba0f3545a5
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487122"
---
# <a name="icon-control"></a>Control de icono

Define un control de icono. Este control es un icono que se muestra en un cuadro de diálogo.

La instrucción de control de **icono** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el identificador de recurso de icono, el identificador de control de icono, la posición y los atributos de un control.

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Nombre de un icono (no un nombre de archivo) definido en otra parte del archivo de recursos.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Ancho*
</dt> <dd>

Este valor se omite y debe establecerse en cero.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*alto*
</dt> <dd>

Este valor se omite y debe establecerse en cero.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilo de control. Este parámetro es opcional. El único valor que se puede especificar es el estilo de **\_ icono de SS** . Este es el estilo predeterminado si este parámetro se especifica o no.

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de icono cuyo identificador de icono es 901 y cuyo nombre es mi Icon:

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ICONO**](icon-resource.md)
</dt> </dl>

 

 




