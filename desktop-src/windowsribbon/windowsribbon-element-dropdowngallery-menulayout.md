---
title: DropDownGallery.MenuLayout, propiedad
description: Representa un contenedor para los diseños de menú desplegable DropDownGallery.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- DropDownGallery.MenuLayout, propiedad Windows Cinta de opciones
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b3fa4c0e2cca92aa2f95f73e0c817314bb71a8260db21a89cb40ec78fff7765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810685"
---
# <a name="dropdowngallerymenulayout-property"></a>DropDownGallery.MenuLayout, propiedad

Representa un contenedor para los diseños de menú desplegable [**DropDownGallery.**](windowsribbon-element-dropdowngallery.md)

## <a name="usage"></a>Uso

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                           | Descripción                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)<br/>         | Debe producirse exactamente una vez<br/> <br/> |
| [**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md)<br/> | Debe producirse exactamente una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                     |
|-----------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**elemento DropDownGallery.**](windowsribbon-element-dropdowngallery.md)

> [!Note]  
> Se permite un máximo de un elemento secundario [**(VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) [**o FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).

En esta sección de código se muestra la declaración de control **DropDownGallery.MenuLayout.**


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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control galería desplegable**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> </dl>

 

 





