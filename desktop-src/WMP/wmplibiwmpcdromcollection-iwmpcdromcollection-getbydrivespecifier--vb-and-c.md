---
title: IWMPCdromCollection getByDriveSpecifier, método
description: El método getByDriveSpecifier devuelve una interfaz IWMPCdrom asociada a una letra de unidad concreta.
ms.assetid: 4a550eb1-a37e-43fd-9e08-801c4fd64e68
keywords:
- método getByDriveSpecifier de Windows Media Player
- método getByDriveSpecifier Windows Media Player, interfaz IWMPCdromCollection
- Interfaz IWMPCdromCollection Windows Media Player, método getByDriveSpecifier
topic_type:
- apiref
api_name:
- IWMPCdromCollection.getByDriveSpecifier
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe771fc893d4bf43b82dc825a2d33724926e8151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718809"
---
# <a name="iwmpcdromcollectiongetbydrivespecifier-method"></a>IWMPCdromCollection:: getByDriveSpecifier (método)

El método **getByDriveSpecifier** devuelve una interfaz **IWMPCdrom** asociada a una letra de unidad concreta.

## <a name="syntax"></a>Sintaxis


```CSharp
public IWMPCdrom getByDriveSpecifier(
  System.String bstrDriveSpecifier
);
```


```VB

Public Function getByDriveSpecifier( _
  ByVal bstrDriveSpecifier As System.String _
) As IWMPCdrom
Implements IWMPCdromCollection.getByDriveSpecifier
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrDriveSpecifier* \[ de\]
</dt> <dd>

**System. String** que es la letra de unidad seguida de un carácter de dos puntos (":").

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una interfaz **WMPLib. IWMPCdrom** .

## <a name="remarks"></a>Observaciones

Las letras de unidad se deben proporcionar con el formato *x*:, donde *x* representa la letra de unidad.

Para usar este método, se requiere acceso de lectura a la biblioteca. Para obtener más información, vea [acceso a la biblioteca](library-access.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **getByDriveSpecifier** para obtener la interfaz **IWMPCdrom** que corresponde a una letra de unidad proporcionada por el usuario en un cuadro de texto. A continuación, se llama al método **IWMPCdrom. EJECT** para expulsar la unidad especificada. El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.


```CSharp
// Store the drive letter provided by the user.
string driveLetter = myText.Text;

// Append a colon to the drive letter to create a valid drive specifier.
driveLetter += ":";

// Get an IWMPCdrom interface for the drive.
WMPLib.IWMPCdrom drive = player.cdromCollection.getByDriveSpecifier(driveLetter);

// Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject();
```


```VB

' Store the drive letter provided by the user.
Dim driveLetter As String = myText.Text

&#39; Append a colon to the drive letter to create a valid drive specifier.
driveLetter += &quot;:&quot;

&#39; Get an IWMPCdrom interface for the drive.
Dim drive As WMPLib.IWMPCdrom = player.cdromCollection.getByDriveSpecifier(driveLetter)

&#39; Use the eject method of the IWMPCdrom interface to open the drive door.
drive.eject()
```





## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versión<br/>   | Windows Media Player 9 series o posterior<br/>                                                                      |
| Espacio de nombres<br/> | **WMPLib**<br/>                                                                                                  |
| Ensamblado<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IWMPCdrom (VB y C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom. EJECT (VB y C#)**](wmplibiwmpcdrom-iwmpcdrom-eject--vb-and-c.md)
</dt> <dt>

[**Interfaz IWMPCdromCollection (VB y C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestMediaAccessRights (VB y C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





