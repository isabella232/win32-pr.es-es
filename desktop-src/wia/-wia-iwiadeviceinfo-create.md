---
description: El método Create del objeto DeviceInfo establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado por el objeto DeviceInfo y devuelve un objeto de elemento que representa el dispositivo.
ms.assetid: 57f3698c-3f9f-4775-8b53-a65a5591aa3d
title: DeviceInfo. Create (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.Create
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1efc36ea8794de4b64c9af616320b09d547f6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720398"
---
# <a name="deviceinfocreate-method"></a>DeviceInfo. Create (método)

El método **Create** del objeto [**DeviceInfo**](-wia-deviceinfo.md) establece una conexión con el dispositivo de adquisición de imágenes de Windows (WIA) especificado por el objeto **DeviceInfo** y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DeviceInfo.Create()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **IWiaDispatchItem**

Este método devuelve el objeto de [**elemento**](-wia-item.md) que representa el dispositivo que se crea.

## <a name="remarks"></a>Observaciones

Use el método **Create** para crear una conexión a un dispositivo de hardware WIA después de enumerar la recopilación de [**dispositivos**](-wia-iwia-devices.md) . El método devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo (un elemento raíz).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso del método **Create** .


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objItem
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objItem = objDeviceInfo.Create()
Next
</SCRIPT>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |



 

 




