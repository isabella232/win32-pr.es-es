---
description: El método Create del objeto WIA establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado y devuelve un objeto de elemento que representa el dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: WIA. Create (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.Create
- SafeWia.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6a388ba2b3ee0506b093221275e34104e3f91bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545558"
---
# <a name="wiacreate-method"></a>WIA. Create (método)

El método **Create** del objeto [**WIA**](-wia-wia.md) establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dispositivo* \[ de de\]
</dt> <dd>

Tipo: **variante \** _

Especifica el dispositivo WIA al que se va a conectar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *IWiaDispatchItem**

Si es correcto, este método devuelve un objeto de [**elemento**](-wia-item.md) que representa un dispositivo de hardware WIA (un elemento raíz).

## <a name="remarks"></a>Observaciones

El parámetro *Device* especifica un objeto [**DeviceInfo**](-wia-deviceinfo.md) pasando el propio objeto, su índice de un objeto de colección o el valor de su propiedad [**ID**](-wia-iwiadeviceinfo-id.md) . No pasar **nada** para mostrar un cuadro de diálogo que permita al usuario seleccionar un dispositivo.

## <a name="examples"></a>Ejemplos

Los siguientes ejemplos de VBScript muestran el uso del método **Create** .

En el primer ejemplo se pasa un objeto [**DeviceInfo**](-wia-deviceinfo.md) al método **Create** . Tenga en cuenta que al pasar la propiedad [**ID**](-wia-iwiadeviceinfo-id.md) del objeto se produce exactamente el mismo comportamiento.


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objWia.Create(objDeviceInfo)
Next
</SCRIPT>
```



En el ejemplo siguiente, la aplicación que realiza la llamada pasa el índice del objeto [**DeviceInfo**](-wia-deviceinfo.md) de la colección al método **Create** .


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objItem
 
Set objWia = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For i = 0 To objDeviceInfoCollection.Count-1
    Set objItem = objWia.Create(i)
Next
</SCRIPT>
```



En el ejemplo siguiente se pasa **Nothing** al método **Create** para mostrar un cuadro de diálogo que permite a un usuario seleccionar un dispositivo.


```JScript
<SCRIPT LANGUAGE = "VBScript">
Dim objWia
Dim objItem
 
Set objWia = objWia.Create(Nothing)
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




