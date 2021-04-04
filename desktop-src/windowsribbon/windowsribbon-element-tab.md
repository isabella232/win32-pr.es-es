---
title: Tab (Elemento)
description: Representa una pestaña principal o contextual.
ms.assetid: 2e73a89c-4d31-4075-93c8-e43213a20791
keywords:
- Barra de herramientas de Windows de elemento de pestaña
topic_type:
- apiref
api_name:
- Tab
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e54abc7e13906ada69c1e10f81878c77c4bf5d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078153"
---
# <a name="tab-element"></a>Tab (Elemento)

Representa una pestaña [principal](windowsribbon-controls-tab.md) o [contextual](windowsribbon-controls-tabgroup.md) .

## <a name="usage"></a>Uso

``` syntax
<Tab
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Tab>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Tipo</th>
<th>Obligatorio</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Válido solo si <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> es el elemento primario.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: String)<br/> </dt> <dd> Una cadena que contiene una lista separada por comas de enteros entre 0 y 31.<br/> El espacio en blanco es válido y se omite.<br/> Longitud máxima: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>XS: positiveInteger o XS: String<br/></td>
<td>No<br/></td>
<td>Asocia el elemento a un <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (XS: positiveInteger o XS: String)<br/> </dt> <dd> Una cadena, un valor entero entre 2 y 59999, ambos incluidos, o un valor hexadecimal entre 0X2 y 0xea5f, ambos incluidos. <br/> El valor debe ser único en el documento XML de la cinta de opciones. <br/> Longitud máxima: 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                         | Descripción                                        |
|---------------------------------------------------------------------------------|----------------------------------------------------|
| [**Group (Grupo)**](windowsribbon-element-group.md)<br/>                         | Puede producirse una o varias veces<br/> <br/> |
| [**TAB. ScalingPolicy**](windowsribbon-element-tab-scalingpolicy.md)<br/> | Puede aparecer como máximo una vez<br/> <br/>      |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                             |
|---------------------------------------------------------------------|
| [**Cinta. pestañas**](windowsribbon-element-ribbon-tabs.md)<br/> |
| [**TabGroup**](windowsribbon-element-tabgroup.md)<br/>       |



## <a name="remarks"></a>Observaciones

Obligatorio.

Debe producirse al menos una vez para cada elemento [**Ribbon. tabs**](windowsribbon-element-ribbon-tabs.md) o [**TabGroup**](windowsribbon-element-tabgroup.md) .

La **pestaña** admite los [modos de aplicación](ribbon-applicationmodes.md).

Si [**ScalingPolicy. IdealSizes**](windowsribbon-element-scalingpolicy-idealsizes.md) está presente para el elemento de **ficha** , se requiere una entrada para cada elemento de [**grupo**](windowsribbon-element-group.md) y su tamaño ideal en **ScalingPolicy. IdealSizes**.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el marcado básico del elemento **Tab** .

En esta sección de código se muestran las declaraciones del comando **Tab** para una pestaña **Inicio** .


```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```



En esta sección de código se muestran las declaraciones de control de **pestaña** .


```XML
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```



## <a name="element-information"></a>Información de elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo compatible<br/> | Windows 7 |
| Puede estar vacío                        | No        |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Control Tab](windowsribbon-controls-tab.md)
</dt> <dt>

[Control de grupo de pestañas](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

