---
title: Propiedad IMsRdpDeviceCollection DeviceByIndex
description: Recupera el dispositivo en el índice especificado.
ms.assetid: fcfc459b-46e1-4f26-a331-745fcf06638b
ms.tgt_platform: multiple
keywords:
- Propiedad DeviceByIndex Servicios de Escritorio remoto
- Propiedad DeviceByIndex Servicios de Escritorio remoto , interfaz IMsRdpDeviceCollection
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto , propiedad DeviceByIndex
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.DeviceByIndex
- IMsRdpDeviceCollection.get_DeviceByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f13279cdf5bed0cd56921dde2344918262abed7e5473290560757e76f4c595c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606444"
---
# <a name="imsrdpdevicecollectiondevicebyindex-property"></a>IMsRdpDeviceCollection::D eviceByIndex

Recupera el dispositivo en el índice especificado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDevice **ppDevice
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero [**de interfaz IMsRdpDevice.**](imsrdpdevice.md)

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

 

 





