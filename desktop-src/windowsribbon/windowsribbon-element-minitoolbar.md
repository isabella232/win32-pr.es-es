---
title: MiniToolbar, elemento
description: Representa una barra de herramientas contextual.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Cinta de opciones de Windows del elemento MiniToolbar
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ceea8ba1a220674f177e740411bf98a13d7bfc2e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443266"
---
# <a name="minitoolbar-element"></a>MiniToolbar, elemento

Representa una barra de herramientas contextual.

## <a name="usage"></a>Uso

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a>Atributos



| Atributo           | Tipo                 | Requerido       | Descripción                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nombre**<br/> | xs:string<br/> | Sí<br/> | <dt> (xs:string)<br/> </dt> <dd> Cadena formada por cualquier secuencia de caracteres, incluidos los caracteres de espacio en blanco y de salto de línea.<br/> </dd> </dl> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Descripción                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**MenuGroup**](windowsribbon-element-menugroup.md)<br/> | Debe producirse al menos una vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse una o varias veces para [**cada ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md).

A diferencia [**del elemento ContextMenu,**](windowsribbon-element-contextmenu.md) **minitoolbar** permanece visible cuando se hace clic en un elemento de la barra de herramientas.

Si se muestra sin [**contextMenu,**](windowsribbon-element-contextmenu.md) **la barra miniherramienta** se atenua cuando se desplaza el puntero del mouse.

> [!Note]  
> Debido a este comportamiento de desvanezco, [**contextMenu**](windowsribbon-element-contextmenu.md) debe mostrarse cerca del puntero del mouse.

 

Dado que los controles de **MiniToolbar** no son accesibles mediante el teclado, los comandos que exponen deben estar disponibles en otra parte de la interfaz de usuario de la cinta de opciones.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para una [**vista ContextPopup.**](windowsribbon-element-contextpopup.md)

En esta sección de código se muestra un conjunto de declaraciones de control **MiniToolbar.**


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a>Información de elemento

* **Sistema mínimo admitido:** Windows 7
* **Puede estar vacío:** No



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control Popup de contexto](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





