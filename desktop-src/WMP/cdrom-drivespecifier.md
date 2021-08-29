---
title: Cdrom.driveSpecifier
description: La propiedad driveSpecifier recupera la letra de unidad de CD o DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Cdrom.driveSpecifier Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a358e54dabf9186dba3a2eb56f38d6fa846aab92f0a8cab6347f568788a1ae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864195"
---
# <a name="cdromdrivespecifier"></a>Cdrom.driveSpecifier

La **propiedad driveSpecifier** recupera la letra de unidad de CD o DVD.

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una cadena de solo **lectura.**

## <a name="remarks"></a>Comentarios

Normalmente, las unidades de DVD pueden reproducir medios de CD, pero las unidades de CD no pueden reproducir medios de DVD. Esta propiedad recupera un especificador de unidad para un índice de unidad de base cero dentro del intervalo recuperado mediante *CdromCollection*. **count**. El valor recuperado tiene la forma *X*:, donde *X* representa la letra de unidad.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

**Reproductor de Windows Media 10 Mobile:** Esta propiedad no se admite.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa Cdrom*. **driveSpecifier para** rellenar un área de texto HTML denominada myText con una lista separada por comas de unidades de CD y DVD disponibles. El **objeto Player** se creó con id. = "Player".


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Reproductor de Windows Media versión 7.0 o posterior<br/>                               |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cdrom (objeto)**](cdrom-object.md)
</dt> <dt>

[**CdromCollection.count**](cdromcollection-count.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





