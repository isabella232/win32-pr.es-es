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
ms.openlocfilehash: c996989661703c4a9c7416cd63904c376fdb7fcca3071d4558551bdd78470d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208791"
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

## <a name="remarks"></a>Comentarios

Use este método para buscar el valor de una propiedad de dispositivo a partir de su identificador. Para obtener una lista de los IDs de propiedad, vea [WiA Property Constant Definitions](-wia-wia-property-constant-definitions.md). Para obtener información sobre Windows propiedades de adquisición de imágenes (WIA), vea WiA Property Constants (Constantes [de propiedad de WIA).](-wia-wia-property-constants.md)

Para las aplicaciones Visual Basic Microsoft, agregue una referencia a "Windows biblioteca de tipos de adquisición de imágenes 1.01". Las siguientes constantes definidas en ese archivo son válidas para este método:

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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




