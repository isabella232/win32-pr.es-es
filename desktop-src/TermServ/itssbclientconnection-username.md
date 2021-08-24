---
title: Propiedad UserName de ITsSbClientConnection
description: Recupera un valor que indica el nombre del usuario que inició la conexión.
ms.assetid: 74f4b8fb-efd4-46d7-9d2f-dd9ef583eb54
ms.tgt_platform: multiple
keywords:
- NombreDeUsuario, propiedad Servicios de Escritorio remoto
- Propiedad UserName Servicios de Escritorio remoto , interfaz ITsSbClientConnection
- Interfaz ITsSbClientConnection Servicios de Escritorio remoto , propiedad UserName
topic_type:
- apiref
api_name:
- ITsSbClientConnection.UserName
- ITsSbClientConnection.get_UserName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6961e6c911b24df2e6c3adbea14b31a2ce8e5a66a9be9082357db957e646a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511335"
---
# <a name="itssbclientconnectionusername-property"></a>Propiedad ITsSbClientConnection::UserName

Recupera un valor que indica el nombre del usuario que inició la conexión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_UserName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un nombre de usuario. Cuando haya terminado de usar la cadena, desconéctela mediante una llamada a la [**función SysFreeString.**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring)

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

 

