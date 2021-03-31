---
title: Propiedad DeviceById de IMsRdpDeviceCollection
description: Recupera el dispositivo con el identificador especificado.
ms.assetid: b64e83fa-5a94-4080-8efa-45cbfe5ceb88
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceById
- Propiedad DeviceById Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceCollection, propiedad DeviceById
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceById
- IMsRdpDeviceCollection.get_DeviceById
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 228e3c7cf03457ca740d4a415257008988215077
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490342"
---
# <a name="imsrdpdevicecollectiondevicebyid-property"></a>IMsRdpDeviceCollection::D propiedad eviceById

Recupera el dispositivo con el identificador especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceById(
  [in]          BSTR devInstanceId,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a la interfaz [**IMsRdpDevice**](imsrdpdevice.md) .

## <a name="error-codes"></a>Códigos de error

Si el método se ejecuta correctamente, se devuelve **S \_ OK** . Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.

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

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





