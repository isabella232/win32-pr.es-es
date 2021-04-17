---
title: CdromCollection. getByDriveSpecifier, método
description: El método getByDriveSpecifier recupera el objeto CDROM asociado a una letra de unidad concreta.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- método getByDriveSpecifier de Windows Media Player
- método getByDriveSpecifier de Windows Media Player, clase CdromCollection
- Clase CdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- CdromCollection.getByDriveSpecifier
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 807b44a7be97ac93b5b0f270c2d1723404887c9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700314"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>CdromCollection. getByDriveSpecifier, método

El método **getByDriveSpecifier** recupera el objeto **CDROM** asociado a una letra de unidad concreta.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*driveSpecifier* \[ de\]
</dt> <dd>

**Cadena** que contiene la letra de unidad seguida de un carácter de dos puntos (":").

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **CDROM** .

## <a name="remarks"></a>Observaciones

Las letras de unidad se deben proporcionar con el formato *x*:, donde *x* representa la letra de unidad.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de JScript se usa *CdromCollection*. **getByDriveSpecifier** para recuperar el objeto **CDROM** que corresponde a una letra de unidad proporcionada por el usuario. Se creó un elemento de texto HTML, con el nombre = "monotext", para los datos proporcionados por el usuario. El objeto **Player** se creó con ID = "Player".


```JScript
// Store the drive letter provided by the user.
var DriveLetter = MyText.value;

// Append a colon to the drive letter to create a valid drive specifier.
DriveLetter += ":";

// Get the Cdrom object using the drive specifier.
var Drive = Player.cdRomCollection.getByDriveSpecifier(DriveLetter);

// Use the Cdrom object to open the drive door.
Drive.eject();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CDROM (objeto)**](cdrom-object.md)
</dt> <dt>

[**CDROM. EJECT**](cdrom-eject.md)
</dt> <dt>

[**Objeto CdromCollection**](cdromcollection-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





