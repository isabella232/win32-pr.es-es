---
description: El método GetPropById del objeto DeviceInfo usa el identificador de una propiedad de dispositivo para devolver su valor.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: DeviceInfo. GetPropById, método
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720539"
---
# <a name="deviceinfogetpropbyid-method"></a>DeviceInfo. GetPropById, método

El método **GetPropById** del objeto [**DEVICEINFO**](-wia-deviceinfo.md) usa el identificador de una propiedad de dispositivo para devolver su valor.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID.* \[ en\]
</dt> <dd>

Tipo: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**

Especifica el identificador de la propiedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **variante**

Este método devuelve el valor de la propiedad especificada por *ID*.

## <a name="remarks"></a>Observaciones

Use este método para buscar el valor de una propiedad de dispositivo de su identificador. Para obtener una lista de identificadores de propiedad, vea [definiciones de constantes de propiedad de WIA](-wia-wia-property-constant-definitions.md). Para obtener información sobre las propiedades de adquisición de imágenes de Windows (WIA), consulte [constantes de propiedad de WIA](-wia-wia-property-constants.md).

En el caso de las aplicaciones de Microsoft Visual Basic, agregue una referencia a "biblioteca de tipos 1,01 de adquisición de imágenes de Windows". Las siguientes constantes definidas en ese archivo son válidas para este método:

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

En el ejemplo siguiente se muestra el uso del método **GetPropById** para recuperar un valor de propiedad.


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




