---
title: Propiedad Ribbon. ApplicationMenu
description: Representa el menú de la aplicación. | Propiedad Ribbon. ApplicationMenu
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Ribbon. ApplicationMenu (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717531"
---
# <a name="ribbonapplicationmenu-property"></a>Propiedad Ribbon. ApplicationMenu

Representa el menú de la aplicación.

## <a name="usage"></a>Uso

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                     | Descripción                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [**ApplicationMenu**](windowsribbon-element-applicationmenu.md)<br/> | Debe aparecer exactamente una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Cinta de opciones**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Observaciones

Obligatorio.

Puede producirse al menos una vez para cada [**cinta**](windowsribbon-element-ribbon.md)de opciones.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para el elemento **Ribbon. ApplicationMenu** .

En esta sección de código se muestra la declaración de control **Ribbon. ApplicationMenu** .


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 





