---
title: Propiedad de dominio ITsSbClientConnection
description: Recupera un valor que indica el nombre de dominio del cliente Conexión a Escritorio remoto (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Propiedades de dominio Servicios de Escritorio remoto
- Propiedad de Servicios de Escritorio remoto , interfaz ITsSbClientConnection
- Interfaz ITsSbClientConnection Servicios de Escritorio remoto , propiedad Domain
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc99724eb419e831e65f402299aa1603be07ab2ab5a88e0ba9b056492514865
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511515"
---
# <a name="itssbclientconnectiondomain-property"></a>Propiedad ITsSbClientConnection::D omain

Recupera un valor que indica el nombre de dominio del cliente Conexión a Escritorio remoto (RDC).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** que contiene el nombre de dominio del cliente RDC. Cuando haya terminado de usar la cadena, desconéctela mediante una llamada a la [**función SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

