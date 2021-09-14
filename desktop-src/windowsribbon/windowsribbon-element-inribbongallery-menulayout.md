---
title: Propiedad InRibbonGallery.MenuLayout
description: Representa un contenedor para los In-Ribbon menú desplegable de la Galería de aplicaciones.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Propiedad InRibbonGallery.MenuLayout Windows Ribbon
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360611"
---
# <a name="inribbongallerymenulayout-property"></a>Propiedad InRibbonGallery.MenuLayout

Representa un contenedor para los [diseños de](windowsribbon-controls-inribbongallery.md) menú desplegable de la Galería de la cinta de opciones.

## <a name="usage"></a>Uso

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
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
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**elemento InRibbonGallery.**](windowsribbon-element-inribbongallery.md)

> [!Note]  
> Se permite un máximo de un elemento secundario [**(VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) [**o FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para la [Galería en la cinta](windowsribbon-controls-inribbongallery.md)de opciones .

En esta sección de código se muestra la declaración de control **InRibbonGallery.MenuLayout.**


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control de la Galería en la cinta de opciones](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Trabajar con galerías](ribbon-controls-galleries.md)
</dt> </dl>

 

 





