---
description: El método GetPropById del objeto DeviceInfo usa el identificador de una propiedad de dispositivo para devolver su valor.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Método DeviceInfo.GetPropById
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571373"
---
# <a name="deviceinfogetpropbyid-method"></a>Método DeviceInfo.GetPropById

El **método GetPropById** del [**objeto DeviceInfo**](-wia-deviceinfo.md) usa el identificador de una propiedad de dispositivo para devolver su valor.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id.* \[ en\]
</dt> <dd>

Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

Especifica el identificador de la propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **VARIANT**

Este método devuelve el valor de la propiedad especificada por *id.*.

## <a name="remarks"></a>Observaciones

Use este método para buscar el valor de una propiedad de dispositivo a partir de su identificador. Para obtener una lista de los iDs de propiedad, vea [Definiciones de constantes de propiedad de WIA.](-wia-wia-property-constant-definitions.md) Para obtener información sobre Windows propiedades de adquisición de imágenes (WIA), vea WiA Property Constants (Constantes [de propiedad de WIA).](-wia-wia-property-constants.md)

Para las aplicaciones Visual Basic Microsoft, agregue una referencia a "biblioteca de tipos Windows image acquisition 1.01". Las siguientes constantes definidas en ese archivo son válidas para este método:

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del **método GetPropById** para recuperar un valor de propiedad.


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




