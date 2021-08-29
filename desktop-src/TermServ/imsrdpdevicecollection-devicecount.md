---
title: IMsRdpDeviceCollection DeviceCount, propiedad
description: Recupera el recuento de objetos de la colección. | IMsRdpDeviceCollection DeviceCount, propiedad
ms.assetid: dc44f3b8-52c4-4e5f-a633-ea7555fd01dd
ms.tgt_platform: multiple
keywords:
- Propiedad DeviceCount Servicios de Escritorio remoto
- Propiedad DeviceCount Servicios de Escritorio remoto , interfaz IMsRdpDeviceCollection
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto , propiedad DeviceCount
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceCount
- IMsRdpDeviceCollection.get_DeviceCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f178cb7dd72ece90a85fe558f371f3d0b63b3c233a1e43054fe4f72f09850003
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033065"
---
# <a name="imsrdpdevicecollectiondevicecount-property"></a>IMsRdpDeviceCollection::D eviceCount

Recupera el recuento de objetos de la colección.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceCount(
  [out] ULONG *pDeviceCount
);
```



## <a name="property-value"></a>Valor de propiedad

Recuento de objetos.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

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

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





