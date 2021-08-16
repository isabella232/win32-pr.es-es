---
title: Método IMsRdpDeviceCollection RescanDevices
description: Actualiza la lista de objetos de la colección. | Método IMsRdpDeviceCollection RescanDevices
ms.assetid: 2e2a959d-0a1d-4aca-9daf-3c24fb9b3b08
ms.tgt_platform: multiple
keywords:
- Método RescanDevices Servicios de Escritorio remoto
- Método RescanDevices Servicios de Escritorio remoto , interfaz IMsRdpDeviceCollection
- Interfaz IMsRdpDeviceCollection Servicios de Escritorio remoto , método RescanDevices
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
ms.openlocfilehash: d62011697b21171f8de326689ca35195ad4057e2e6edd01a5159fcf89c32d0f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959245"
---
# <a name="imsrdpdevicecollectionrescandevices-method"></a>IMsRdpDeviceCollection::RescanDevices (método)

Actualiza la lista de objetos de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RescanDevices(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vboolDynRedir* \[ En\]
</dt> <dd>

El estado de redireccionamiento predeterminado que se aplicará a los dispositivos o unidades recién detectados.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID IMsRdpDeviceCollection se define como \_ 56540617-d281-488c-8738-6a8fdf64a118<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpDeviceCollection**](imsrdpdevicecollection.md)
</dt> </dl>

 

 





