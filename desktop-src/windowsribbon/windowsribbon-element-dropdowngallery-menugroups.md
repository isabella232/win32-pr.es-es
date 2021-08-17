---
title: DropDownGallery.MenuGroups, propiedad
description: Representa un contenedor para un conjunto de elementos de menú desplegable en un control Drop-Down galería.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- DropDownGallery.MenuGroups, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdc52877884ac3a6407a0c7ed9f511cf78f8bcb5c125beb5f2ed19e651b83da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119393064"
---
# <a name="dropdowngallerymenugroups-property"></a>DropDownGallery.MenuGroups, propiedad

Representa un contenedor para un conjunto de elementos de menú desplegable en un control [Galería desplegable.](windowsribbon-controls-dropdowngallery.md)

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
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Debe producirse al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Comentarios

Obligatorio.

Debe producirse exactamente una vez [**para cada elemento DropDownGallery.**](windowsribbon-element-dropdowngallery.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para **el elemento DropDownGallery.MenuGroups.**

En esta sección de código se muestra la declaración de control **DropDownGallery.MenuGroups** en un espacio de comandos [de la galería](windowsribbon-controls-dropdowngallery.md) desplegable.


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Control galería desplegable**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> </dl>

 

 





