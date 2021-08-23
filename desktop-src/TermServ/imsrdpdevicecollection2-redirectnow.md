---
title: Método IMsRdpDeviceCollection2 RedirectNow
description: Obliga a que los dispositivos seleccionados o no seleccionados de la colección se redirijan o quiten.
ms.assetid: 9cd5849d-a589-43f3-b904-6b2e15ca033d
ms.tgt_platform: multiple
keywords:
- Método redirectNow Servicios de Escritorio remoto
- Método RedirectNow Servicios de Escritorio remoto , interfaz IMsRdpDeviceCollection2
- Interfaz IMsRdpDeviceCollection2 Servicios de Escritorio remoto , método RedirectNow
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
ms.openlocfilehash: 60c92eff142305e95a71c69cdce9789b0d2316e3d5e60b703a7c1aa8e835688f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058923"
---
# <a name="imsrdpdevicecollection2redirectnow-method"></a>IMsRdpDeviceCollection2::RedirectNow (método)

Obliga a que los dispositivos seleccionados o no seleccionados de la colección se redirijan o quiten.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RedirectNow(
  [in] RedirectDeviceType Type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tipo* \[ En\]
</dt> <dd>

Tipo: **[ **RedirectDeviceType**](redirectdevicetype.md)**

Valor de la [**enumeración RedirectDeviceType**](redirectdevicetype.md) que especifica el tipo de dispositivo que se va a redirigir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

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

 

 





