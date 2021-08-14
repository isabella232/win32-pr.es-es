---
title: Propiedad Command.LargeHighContrastImages
description: Representa un contenedor de imágenes; En este caso, imágenes grandes para su uso con la configuración del sistema de contraste alto.
ms.assetid: e25f207f-ac3f-4a5f-8104-c928b38a52a8
keywords:
- Command.LargeHighContrastImages, propiedad Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.LargeHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59c1e760565443c286969cc92b3b0c4a6b83a2513587f424ebcda366b1b8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710515"
---
# <a name="commandlargehighcontrastimages-property"></a>Propiedad Command.LargeHighContrastImages

Representa un contenedor de imágenes; En este caso, imágenes grandes para su uso con la configuración del sistema de contraste alto.

## <a name="usage"></a>Uso

``` syntax
<Command.LargeHighContrastImages>
  child elements
</Command.LargeHighContrastImages>
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

Los recursos de imagen deben cumplir el formato de gráfico estándar de mapa de bits (BMP) que se usa en Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**SplitButton**](windowsribbon-element-splitbutton.md) con un [**elemento MenuGroup.**](windowsribbon-element-menugroup.md)

En esta sección de código se muestran las declaraciones de los comandos [**SplitButton**](windowsribbon-element-splitbutton.md) y [**MenuGroup**](windowsribbon-element-menugroup.md) con recursos de imagen de contraste alto grandes y pequeños. También se [**declara**](windowsribbon-element-group.md) un grupo asociado que actúa como contenedor primario para el elemento **SplitButton.**


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Especificar recursos de imagen de cinta de opciones](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 





