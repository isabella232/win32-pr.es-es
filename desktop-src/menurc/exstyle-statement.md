---
title: EXSTYLE, instrucción
description: Define estilos de ventana extendidos para un cuadro de diálogo. En una definición de recurso, la instrucción EXSTYLE se coloca con las instrucciones opcionales antes del principio del cuerpo de la definición de recurso.
ms.assetid: 5dc74bab-e385-457c-80c4-5e04eed589b5
keywords:
- Menús de instrucciones EXSTYLE y otros recursos
topic_type:
- apiref
api_name:
- EXSTYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 277727757daeaafe5ad11cfd2e4f5fb6ee726458
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252417"
---
# <a name="exstyle-statement"></a>EXSTYLE, instrucción

Define estilos de ventana extendidos para un cuadro de diálogo. En una definición de recurso, la **instrucción EXSTYLE** se coloca con las instrucciones opcionales antes del principio del cuerpo de la definición de recurso.

``` syntax
EXSTYLE extended-style
```

<dl> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*estilo extendido*
</dt> <dd>

Estilo de ventana extendido para el cuadro de diálogo o control. Para obtener una lista de estilos de ventana extendidos, vea [**Estilos de ventana extendidos.**](/windows/desktop/winmsg/extended-window-styles)

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para los controles, los estilos extendidos se especifican después de la *opción style* en la instrucción resource-definition del control. Para más información, consulte la instrucción de definición de recursos para el control individual.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> <dt>

[**MENÚ**](menu-resource.md)
</dt> <dt>

[**POPUP**](popup-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[Recurso definido por el usuario](user-defined-resource.md)
</dt> </dl>

 

 