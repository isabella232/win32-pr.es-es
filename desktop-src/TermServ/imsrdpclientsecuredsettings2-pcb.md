---
title: IMsRdpClientSecuredSettings2 (propiedad de PCB)
description: Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor. | IMsRdpClientSecuredSettings2 (propiedad de PCB)
ms.assetid: e2ddd9fd-d868-4fc5-835d-0f4db5da71e3
ms.tgt_platform: multiple
keywords:
- Propiedad PCB Servicios de Escritorio remoto
- Propiedad PCB Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings2, propiedad PCB
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings2.PCB
- IMsRdpClientSecuredSettings2.get_PCB
- IMsRdpClientSecuredSettings2.put_PCB
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99b9a04a854f218fcbe1735ec6271aa4a58edba
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678751"
---
# <a name="imsrdpclientsecuredsettings2pcb-property"></a>IMsRdpClientSecuredSettings2::P propiedad CB

Especifica la configuración del BLOB de preconexión (PCB) que se va a usar antes de la conexión para la transmisión al servidor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_PCB(
  [in]          BSTR bstrPCB
);

HRESULT get_PCB(
  [out, retval] BSTR *bstrPCB
);
```



## <a name="property-value"></a>Valor de propiedad

La configuración de PCB.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md)
</dt> </dl>

 

 





