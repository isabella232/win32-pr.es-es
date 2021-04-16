---
title: Interfaz IMsRdpDeviceV2
description: Contiene información sobre un objeto de dispositivo. Se trata de una mejora de la interfaz IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, descrito
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685852"
---
# <a name="imsrdpdevicev2-interface"></a>Interfaz IMsRdpDeviceV2

Contiene información sobre un objeto de dispositivo. Se trata de una mejora de la interfaz [**IMsRdpDevice**](imsrdpdevice.md) .

## <a name="members"></a>Miembros

La interfaz **IMsRdpDeviceV2** hereda de [**IMsRdpDevice**](imsrdpdevice.md). **IMsRdpDeviceV2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpDeviceV2** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso          | Descripción                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**CmClassGuid**](imsrdpdevicev2-cmclassguid.md)<br/>             | Solo lectura<br/> | Contiene el GUID de la clase de instalación de Configuration Manager para el dispositivo.<br/>                     |
| [**CmDeviceInstance**](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | Solo lectura<br/> | Contiene la instancia de dispositivo de Configuration Manager del dispositivo.<br/>                       |
| [**DeviceText**](imsrdpdevicev2-devicetext.md)<br/>               | Solo lectura<br/> | Contiene el texto del dispositivo.<br/>                                                               |
| [**DriveLetterBitmap**](imsrdpdevicev2-driveletterbitmap.md)<br/> | Solo lectura<br/> | Contiene un campo de bits que representa una asignación de Letras de unidad incluidas en el dispositivo.<br/> |
| [**IsCompositeDevice**](imsrdpdevicev2-iscompositedevice.md)<br/> | Solo lectura<br/> | Especifica si el dispositivo es un dispositivo compuesto.<br/>                                          |
| [**IsOptionalDevice**](imsrdpdevicev2-isoptionaldevice.md)<br/>   | Solo lectura<br/> | Especifica si el dispositivo es opcional para el redireccionamiento USB.<br/>                                |
| [**IsUSBDevice**](imsrdpdevicev2-isusbdevice.md)<br/>             | Solo lectura<br/> | Especifica si el dispositivo es para el redireccionamiento USB.<br/>                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 con SP1<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2 con SP1<br/>                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



 

 





