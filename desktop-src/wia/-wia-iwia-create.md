---
description: El método Create del objeto Wia establece una conexión con el dispositivo Windows Image Acquisition (WIA) especificado y devuelve un objeto Item que representa el dispositivo.
ms.assetid: c33c635a-159c-4ac3-8ad5-6f21a1986702
title: Método Wia.Create
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
ms.openlocfilehash: a4056354992010d3d213ed619b7460e12c800630ca38fb17acb6d7677fe842a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814055"
---
# <a name="wiacreate-method"></a>Método Wia.Create

El **método Create** del objeto [**Wia**](-wia-wia.md) establece una conexión con el dispositivo Windows Image Acquisition (WIA) especificado y devuelve un objeto [**Item**](-wia-item.md) que representa el dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Wia.Create(
  Device
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dispositivo* \[ En\]
</dt> <dd>

Tipo: **\* VARIANT**

Especifica el dispositivo WIA al que se va a conectar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **IWiaDispatchItem**

Si se realiza correctamente, este método devuelve un [**objeto Item**](-wia-item.md) que representa un dispositivo de hardware WIA (un elemento raíz).

## <a name="remarks"></a>Comentarios

El *parámetro Device* especifica un objeto [**DeviceInfo**](-wia-deviceinfo.md) pasando el propio objeto, su índice de un objeto de colección o el valor de su [**propiedad Id.**](-wia-iwiadeviceinfo-id.md) Pasar **nada** para mostrar un cuadro de diálogo que permite a un usuario seleccionar un dispositivo.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos de VBScript se muestra el uso del **método Create.**

En el primer ejemplo se pasa [**un objeto DeviceInfo**](-wia-deviceinfo.md) al **método Create.** Tenga en cuenta que pasar la propiedad [**Id**](-wia-iwiadeviceinfo-id.md) del objeto produce exactamente el mismo comportamiento.


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



En el ejemplo siguiente, la aplicación que realiza la llamada pasa el índice del [**objeto DeviceInfo**](-wia-deviceinfo.md) de la colección al **método Create.**


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



En el ejemplo siguiente se **pasa Nothing** al **método Create** para mostrar un cuadro de diálogo que permite a un usuario seleccionar un dispositivo.


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4.90 o posterior)</dt> </dl> |



 

 




