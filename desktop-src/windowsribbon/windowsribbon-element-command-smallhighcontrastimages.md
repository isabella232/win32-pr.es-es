---
title: Propiedad Command.SmallHighContrastImages
description: Representa un contenedor de imágenes; en este caso, imágenes pequeñas para su uso con la configuración del sistema de contraste alto.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- Propiedad Command.SmallHighContrastImages Windows cinta de opciones
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56291ad4e56e5f941fe4cb2790ac6afab27ad67b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247491"
---
# <a name="commandsmallhighcontrastimages-property"></a>Propiedad Command.SmallHighContrastImages

Representa un contenedor de imágenes; en este caso, imágenes pequeñas para su uso con la configuración del sistema de contraste alto.

## <a name="usage"></a>Uso

``` syntax
<Command.SmallHighContrastImages>
  child elements
</Command.SmallHighContrastImages>
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
| [**Comando**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse como máximo una vez para cada [**comando**](windowsribbon-element-command.md).

Los recursos de imagen deben ajustarse al formato de gráfico de mapa de bits estándar (BMP) que se usa en Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**SplitButton**](windowsribbon-element-splitbutton.md) con un [**elemento MenuGroup.**](windowsribbon-element-menugroup.md)

En esta sección de código se muestran las [**declaraciones SplitButton**](windowsribbon-element-splitbutton.md) [**y MenuGroup**](windowsribbon-element-menugroup.md) Command con recursos grandes y pequeños de imágenes de contraste alto. También se [**declara**](windowsribbon-element-group.md) un grupo asociado que actúa como contenedor primario para el elemento **SplitButton.**


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
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Especificar recursos de imagen de cinta de opciones](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





