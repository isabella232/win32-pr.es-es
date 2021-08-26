---
title: Propiedad IMsRdpClient9 TransportSettings4
description: Recupera un objeto que admite la interfaz IMsRdpClientTransportSettings4.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- Propiedad TransportSettings4 Servicios de Escritorio remoto
- Propiedad TransportSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto , propiedad TransportSettings4
- Propiedad TransportSettings4 Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , propiedad TransportSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bf5c8d4371b6e4357fdeca21ba78265af8bb345f851e8d15a0eb01317fb6f51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990295"
---
# <a name="imsrdpclient9transportsettings4-property"></a>Propiedad IMsRdpClient9::TransportSettings4

Recupera un objeto que admite la [**interfaz IMsRdpClientTransportSettings4.**](imsrdpclienttransportsettings4.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve un [**puntero de interfaz IMsRdpClientTransportSettings4.**](imsrdpclienttransportsettings4.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> IID IMsRdpClient9 se define como \_ 28904001-04B6-436C-A55B-0AF1A0883DC9<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





