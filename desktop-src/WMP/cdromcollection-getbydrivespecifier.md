---
title: Método CdromCollection.getByDriveSpecifier
description: El método getByDriveSpecifier recupera el objeto Cdrom asociado a una letra de unidad determinada.
ms.assetid: 60626ffc-3d10-435b-8827-c5d7b6e02607
keywords:
- Método getByDriveSpecifier Reproductor de Windows Media
- Método getByDriveSpecifier Reproductor de Windows Media , clase CdromCollection
- Método cdromCollection Reproductor de Windows Media , getByDriveSpecifier
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
ms.openlocfilehash: fa5487b3a57fb1e7e4167561fcca08e10d6472182881fa221bd8e671bc814cc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864095"
---
# <a name="cdromcollectiongetbydrivespecifier-method"></a>Método CdromCollection.getByDriveSpecifier

El **método getByDriveSpecifier** recupera el **objeto Cdrom** asociado a una letra de unidad determinada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = CdromCollection.getByDriveSpecifier(
  driveSpecifier
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*driveSpecifier* \[ En\]
</dt> <dd>

**Cadena** que contiene la letra de unidad seguida de un carácter de dos puntos (":").

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **objeto Cdrom.**

## <a name="remarks"></a>Comentarios

Las letras de unidad deben proporcionarse con el *formato X*:, donde *X* representa la letra de unidad.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [Acceso a la biblioteca](library-access.md).

**Reproductor de Windows Media 10 Mobile:** No se admite este método.

## <a name="examples"></a>Ejemplos

En el ejemplo JScript siguiente se *usa CdromCollection*. **getByDriveSpecifier para** recuperar el **objeto Cdrom** que corresponde a una letra de unidad proporcionada por el usuario. Se creó un elemento de texto HTML, con NAME = "MyText", para la entrada del usuario. El **objeto Player** se creó con id. = "Player".


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
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Cdrom (objeto)**](cdrom-object.md)
</dt> <dt>

[**Cdrom.eject**](cdrom-eject.md)
</dt> <dt>

[**CdromCollection (objeto)**](cdromcollection-object.md)
</dt> <dt>

[**Configuración.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configuración.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





