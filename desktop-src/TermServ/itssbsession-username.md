---
title: Propiedad De nombre de usuario de ITsSbSession
description: Recupera el nombre de usuario de esta sesión.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Nombre de usuario, propiedad Servicios de Escritorio remoto
- Propiedad Username Servicios de Escritorio remoto , interfaz ITsSbSession
- Interfaz ITsSbSession Servicios de Escritorio remoto , propiedad Username
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60d42c06d700cb95df5635f902876c242b164a6fd12415848cc11539cb30edd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351205"
---
# <a name="itssbsessionusername-property"></a>Propiedad ITsSbSession::Username

Recupera el nombre de usuario de esta sesión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** que recibe el nombre de usuario de esta sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





