---
title: IMsRdpDeviceCollection2 RedirectNow, método
description: Fuerza la redirección o eliminación de los dispositivos que se seleccionaron o anularon de la colección.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Método RedirectNow Servicios de Escritorio remoto
- Método RedirectNow Servicios de Escritorio remoto, interfaz IMsRdpDeviceCollection2
- Interfaz IMsRdpDeviceCollection2 Servicios de Escritorio remoto, método RedirectNow
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2.RedirectNow
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 893d1e26f504d5aeb45f795ea7425eeefc3a6232
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995945"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>IMsRdpDeviceCollection2:: RedirectNow (método)

Fuerza la redirección o eliminación de los dispositivos que se seleccionaron o anularon de la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* \[ de de\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Un valor de la enumeración [**RedirectDeviceType**](redirectdevicetype.md) que especifica el tipo de dispositivo que se va a redirigir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RedirectDeviceType**](redirectdevicetype.md)
</dt> <dt>

[**IMsRdpDeviceCollection2**](imsrdpdevicecollection2.md)
</dt> </dl>

 

 





