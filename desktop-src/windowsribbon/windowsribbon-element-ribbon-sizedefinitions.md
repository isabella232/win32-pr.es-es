---
title: Propiedad Ribbon. SizeDefinitions
description: Representa un contenedor para plantillas de diseño personalizado de controles de la cinta de opciones.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Ribbon. SizeDefinitions (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078954"
---
# <a name="ribbonsizedefinitions-property"></a>Propiedad Ribbon. SizeDefinitions

Representa un contenedor para plantillas de diseño personalizado de controles de la cinta de opciones.

## <a name="usage"></a>Uso

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                   | Descripción                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [**SizeDefinition**](windowsribbon-element-sizedefinition.md)<br/> | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra una plantilla personalizada básica.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Personalización de una cinta a través de definiciones de tamaño y directivas de escalado](windowsribbon-templates.md)
</dt> </dl>

 

 





