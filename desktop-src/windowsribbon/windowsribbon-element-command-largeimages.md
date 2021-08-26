---
title: Propiedad Command.LargeImages
description: Representa un contenedor de imágenes; En este caso, imágenes grandes.
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- Command.LargeImages, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66214eb05910296b2c03a749d88134bef68f86badc2ffd7f7b69d0ba6adfdd5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931625"
---
# <a name="commandlargeimages-property"></a>Propiedad Command.LargeImages

Representa un contenedor de imágenes; En este caso, imágenes grandes.

## <a name="usage"></a>Uso

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                 | Descripción                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Imagen**](windowsribbon-element-image.md)<br/> | Puede producirse una o varias veces<br/> <br/> |



## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                     |
|-------------------------------------------------------------|
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Comentarios

Opcional.

Puede producirse como máximo una vez para cada [**comando**](windowsribbon-element-command.md).

Los recursos de imagen deben ajustarse al formato de gráfico estándar de mapa de bits (BMP) que se usa Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**SplitButton**](windowsribbon-element-splitbutton.md) con un [**elemento MenuGroup.**](windowsribbon-element-menugroup.md)

En esta sección de código se muestran las [**declaraciones de**](windowsribbon-element-splitbutton.md) los comandos SplitButton y [**MenuGroup**](windowsribbon-element-menugroup.md) con un recurso de imagen grande y pequeño. También se [**declara**](windowsribbon-element-group.md) un grupo asociado que actúa como contenedor primario para el elemento **SplitButton.**


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Especificar recursos de imagen de cinta de opciones](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ LargeImage](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 





