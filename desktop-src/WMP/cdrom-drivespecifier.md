---
title: CDROM. driveSpecifier
description: La propiedad driveSpecifier recupera la letra de unidad de CD o DVD.
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- Media Player de Windows de CDROM. driveSpecifier
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
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533909"
---
# <a name="cdromdrivespecifier"></a>CDROM. driveSpecifier

La propiedad **driveSpecifier** recupera la letra de unidad de CD o DVD.

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a>Valores posibles

Esta propiedad es una **cadena** de solo lectura.

## <a name="remarks"></a>Observaciones

Normalmente, las unidades de DVD pueden reproducir un CD, pero las unidades de CD no pueden reproducir medios de DVD. Esta propiedad recupera un especificador de unidad para un índice de unidad de base cero dentro del intervalo recuperado mediante *CdromCollection*. **recuento**. El valor recuperado toma la forma *x*:, donde *X* representa la letra de unidad.

Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Esta propiedad no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa el *CDROM*. **driveSpecifier** para rellenar un área de texto HTML denominada mi texto con una lista separada por comas de unidades de CD y DVD disponibles. El objeto **Player** se creó con ID = "Player".


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Versión<br/>                  | Windows Media Player versión 7,0 o posterior<br/>                               |
| Archivo DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDROM (objeto)**](cdrom-object.md)
</dt> <dt>

[**CdromCollection. Count**](cdromcollection-count.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





