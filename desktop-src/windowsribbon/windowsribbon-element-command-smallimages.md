---
title: Propiedad Command.SmallImages
description: Representa un contenedor de imágenes; En este caso, imágenes pequeñas.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Propiedad Command.SmallImages Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63445f2dbfce88e9793b3563d0ce8ed9861f45fa0831680a455b1a0a04bb4bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329275"
---
# <a name="commandsmallimages-property"></a>Propiedad Command.SmallImages

Representa un contenedor de imágenes; En este caso, imágenes pequeñas.

## <a name="usage"></a>Uso

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
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

Los recursos de imagen deben ajustarse al formato de gráfico de mapa de bits estándar (BMP) que se usa en Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**SplitButton**](windowsribbon-element-splitbutton.md) con un [**elemento MenuGroup.**](windowsribbon-element-menugroup.md)

En esta sección de código se muestran [**las declaraciones SplitButton**](windowsribbon-element-splitbutton.md) [**y MenuGroup**](windowsribbon-element-menugroup.md) Command con un recurso de imagen grande y pequeño. También se [**declara**](windowsribbon-element-group.md) un grupo asociado que actúa como contenedor primario para el elemento **SplitButton.**


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

[UI \_ PKEY \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





