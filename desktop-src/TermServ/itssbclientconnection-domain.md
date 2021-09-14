---
title: Propiedad de dominio ITsSbClientConnection
description: Recupera un valor que indica el nombre de dominio del Conexión a Escritorio remoto (RDC).
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
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168638"
---
# <a name="itssbclientconnectiondomain-property"></a>Propiedad ITsSbClientConnection::D omain

Recupera un valor que indica el nombre de dominio del Conexión a Escritorio remoto (RDC).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** que contiene el nombre de dominio del cliente RDC. Cuando haya terminado de usar la cadena, descálala mediante una llamada a la [**función SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

