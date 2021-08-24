---
title: QuickAccessToolbar.ApplicationDefaults, propiedad
description: Representa un contenedor para los comandos predeterminados en la barra de herramientas de acceso rápido (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- QuickAccessToolbar.ApplicationDefaults, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701a7c72e40b1efe9104d6794fa739c556b0fb4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473751"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>QuickAccessToolbar.ApplicationDefaults, propiedad

Representa un contenedor para los comandos predeterminados en la [barra de herramientas de acceso rápido (QAT).](windowsribbon-controls-quickaccesstoolbar.md)

## <a name="usage"></a>Uso

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios




| Elemento | Descripción | 
|---------|-------------|
| <a href="windowsribbon-element-button.md"><strong>Botón</strong></a><br /> | Debe aparecer al menos una vez.<br /><br /> | 
| <a href="windowsribbon-element-checkbox.md"><strong>Casilla</strong></a><br /> | Debe aparecer al menos una vez.<br /><br /> | 
| <a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br /> | Debe aparecer al menos una vez.<br /><blockquote>[!Note]<br />Windows 8 y versiones más recientes.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br /> | Debe aparecer al menos una vez.<br /><blockquote>[!Note]<br />Windows 8 y versiones más recientes.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br /> | Debe aparecer al menos una vez.<br /><blockquote>[!Note]<br />Windows 8 y versiones más recientes.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br /> | Debe aparecer al menos una vez.<br /><blockquote>[!Note]<br />Windows 8 y versiones más recientes.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br /> | Debe aparecer al menos una vez.<br /><br /> | 




## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para [**cada QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Se debe especificar un mínimo de un elemento secundario.

Se puede especificar un máximo de 20 elementos secundarios.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

En esta sección de código se muestra la declaración de control **QuickAccessToolbar.ApplicationDefaults.**


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





