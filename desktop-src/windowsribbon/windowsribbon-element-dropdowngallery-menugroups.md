---
title: Propiedad DropDownGallery. MenuGroups
description: Representa un contenedor para un conjunto de elementos de menú desplegable en un control de la galería de Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- DropDownGallery. MenuGroups (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720230"
---
# <a name="dropdowngallerymenugroups-property"></a>Propiedad DropDownGallery. MenuGroups

Representa un contenedor para un conjunto de elementos de menú desplegable en un control de la [Galería](windowsribbon-controls-dropdowngallery.md) desplegable.

## <a name="usage"></a>Uso

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Descripción                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Debe aparecer al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Debe aparecer exactamente una vez para cada elemento [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el elemento **DropDownGallery. MenuGroups** .

En esta sección de código se muestra la declaración de control **DropDownGallery. MenuGroups** en un espacio de comandos de la [Galería](windowsribbon-controls-dropdowngallery.md) desplegable.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control Galería desplegable**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> </dl>

 

 





