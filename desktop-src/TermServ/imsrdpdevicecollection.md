---
title: IMsRdpDeviceCollection (interfaz)
description: Representa una colección de objetos de dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto , descrito
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
ms.openlocfilehash: c5f7008b0b524150cd106b9bbe97d21a8de890773d8b0b461a6ae3045e847a79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000745"
---
# <a name="imsrdpdevicecollection-interface"></a>IMsRdpDeviceCollection (interfaz)

Representa una colección de objetos de dispositivo.

## <a name="members"></a>Miembros

La **interfaz IMsRdpDeviceCollection** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDeviceCollection** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpDeviceCollection** tiene estos métodos.



| Método                                                        | Descripción                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [**Volver a examinarDispositivos**](imsrdpdevicecollection-rescandevices.md) | Actualiza la lista de objetos de la colección.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpDeviceCollection** tiene estas propiedades.



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
| IID<br/>                      | IID IMsRdpDeviceCollection se define como \_ 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDevice**](imsrdpdevice.md)
</dt> </dl>

 

