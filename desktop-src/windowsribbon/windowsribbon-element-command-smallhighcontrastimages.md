---
title: Command. SmallHighContrastImages (propiedad)
description: Representa un contenedor de imágenes; en este caso, imágenes pequeñas para su uso con la configuración del sistema de alto contraste.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- Command. SmallHighContrastImages (propiedad) cinta de Windows
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56291ad4e56e5f941fe4cb2790ac6afab27ad67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676903"
---
# <a name="commandsmallhighcontrastimages-property"></a>Command. SmallHighContrastImages (propiedad)

Representa un contenedor de imágenes; en este caso, imágenes pequeñas para su uso con la configuración del sistema de alto contraste.

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
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Observaciones

Opcional.

Puede producirse al menos una vez para cada [**comando**](windowsribbon-element-command.md).

Los recursos de imagen deben cumplir el formato de gráficos de mapa de bits estándar (BMP) usado en Windows.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el marcado básico para [**splitButton**](windowsribbon-element-splitbutton.md) con un elemento [**MenuGroup**](windowsribbon-element-menugroup.md) .

En esta sección de código se muestran las declaraciones de comandos [**splitButton**](windowsribbon-element-splitbutton.md) y [**MenuGroup**](windowsribbon-element-menugroup.md) con recursos grandes y pequeños de imagen de contraste alto. También se declara un [**Grupo**](windowsribbon-element-group.md) asociado que actúa como contenedor primario para el elemento **splitButton** .


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Especificar recursos de imagen de cinta](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ SmallHighContrastImage](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





