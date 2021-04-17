---
title: IMsRdpDeviceCollection RescanDevices, método
description: Actualiza la lista de objetos de la colección. | IMsRdpDeviceCollection RescanDevices, método
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Método RescanDevices Servicios de Escritorio remoto
- Método RescanDevices Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto, método RescanDevices
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection.RescanDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 773231ffd89a0998f6073f844a3f974920625987
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678735"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>IMsRdpDeviceCollection:: RescanDevices (método)

Actualiza la lista de objetos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vboolDynRedir* \[ de\]
</dt> <dd>

El estado de redirección predeterminada que se aplicará a los dispositivos o unidades recién detectados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

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

 

 





