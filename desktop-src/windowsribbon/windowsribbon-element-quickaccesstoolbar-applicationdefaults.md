---
title: Propiedad QuickAccessToolbar. ApplicationDefaults
description: Representa un contenedor para los comandos predeterminados en la barra de herramientas de acceso rápido (QAT).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- QuickAccessToolbar. ApplicationDefaults (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 084ea334441cb0cf545adaa3d1016f7d02da1b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705122"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>Propiedad QuickAccessToolbar. ApplicationDefaults

Representa un contenedor para los comandos predeterminados en la [barra de herramientas de acceso rápido (Qat)](windowsribbon-controls-quickaccesstoolbar.md).

## <a name="usage"></a>Uso

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-button.md"><strong>Botón</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-checkbox.md"><strong>CheckBox</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 y versiones más recientes.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 y versiones más recientes.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 y versiones más recientes.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/>
<blockquote>
[!Note]<br />
Windows 8 y versiones más recientes.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br/></td>
<td>Debe aparecer al menos una vez.<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

Se debe especificar un mínimo de un elemento secundario.

Se puede especificar un máximo de 20 elementos secundarios.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md).

En esta sección de código se muestra la declaración de control **QuickAccessToolbar. ApplicationDefaults** .


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de barra de herramientas de acceso rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





