---
title: Propiedad de dominio ITsSbClientConnection
description: Recupera un valor que indica el nombre de dominio del cliente Conexión a Escritorio remoto (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedad de dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz ITsSbClientConnection
- Servicios de Escritorio remoto de la interfaz ITsSbClientConnection, propiedad del dominio
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686170"
---
# <a name="itssbclientconnectiondomain-property"></a>ITsSbClientConnection::D propiedad omain

Recupera un valor que indica el nombre de dominio del cliente Conexión a Escritorio remoto (RDC).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a una variable **BSTR** que contiene el nombre de dominio del cliente RDC. Cuando haya terminado de usar la cadena, puede liberarla llamando a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

