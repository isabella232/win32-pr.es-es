---
title: EQUALIZERSETTINGS.nextPreset
description: El método nextPreset aplica el siguiente valor preestablecido del ecualizador.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS. nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700281"
---
# <a name="equalizersettingsnextpreset"></a>EQUALIZERSETTINGS.nextPreset

El método **nextPreset** aplica el siguiente valor preestablecido del ecualizador.

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el valor predeterminado actual es el último disponible, el primer valor preestablecido se convierte en actual.

## <a name="examples"></a>Ejemplos


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.previousPreset**](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





