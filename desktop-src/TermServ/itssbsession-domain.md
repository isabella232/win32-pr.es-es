---
title: Propiedad de dominio ITsSbSession
description: Recupera el nombre de dominio del usuario.
ms.assetid: bbb9a805-7270-4555-8fee-130a46bc3903
ms.tgt_platform: multiple
keywords:
- Propiedades de dominio Servicios de Escritorio remoto
- Propiedad de Servicios de Escritorio remoto , interfaz ITsSbSession
- Interfaz ITsSbSession Servicios de Escritorio remoto , propiedad Domain
topic_type:
- apiref
api_name:
- ITsSbSession.Domain
- ITsSbSession.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52854f719830933c96bc130dbec4f0b15f1264344396382ad59099d4c37cf02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128310"
---
# <a name="itssbsessiondomain-property"></a>Propiedad ITsSbSession::D omain

Recupera el nombre de dominio del usuario.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Domain(
  [out, retval] BSTR *domain
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** que recibe el nombre de dominio del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





