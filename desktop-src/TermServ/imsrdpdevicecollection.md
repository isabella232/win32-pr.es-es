---
title: Interfaz IMsRdpDeviceCollection
description: Representa una colección de objetos de dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection, descrito
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421925"
---
# <a name="imsrdpdevicecollection-interface"></a>Interfaz IMsRdpDeviceCollection

Representa una colección de objetos de dispositivo.

## <a name="members"></a>Miembros

La interfaz **IMsRdpDeviceCollection** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDeviceCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpDeviceCollection** tiene estos métodos.



| Método                                                        | Descripción                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDevices**](imsrdpdevicecollection-rescandevices.md) | Actualiza la lista de objetos de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpDeviceCollection** tiene estas propiedades.



| Propiedad                                                                 | Tipo de acceso          | Descripción                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [**DeviceById**](imsrdpdevicecollection-devicebyid.md)<br/>       | Solo lectura<br/> | Recupera el dispositivo con el identificador especificado.<br/> |
| [**DeviceByIndex**](imsrdpdevicecollection-devicebyindex.md)<br/> | Solo lectura<br/> | Recupera el dispositivo en el índice especificado.<br/>        |
| [**DeviceCount**](imsrdpdevicecollection-devicecount.md)<br/>     | Solo lectura<br/> | Recupera el recuento de objetos de la colección.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsRdpDeviceCollection se define como 56540617-D281-488C-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

