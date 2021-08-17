---
title: Propiedad TargetName de ITsSbSession
description: Recupera el nombre del destino en el que se creó esta sesión.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Propiedad TargetName Servicios de Escritorio remoto
- Propiedad TargetName Servicios de Escritorio remoto , interfaz ITsSbSession
- Interfaz ITsSbSession Servicios de Escritorio remoto , propiedad TargetName
topic_type:
- apiref
api_name:
- ITsSbSession.TargetName
- ITsSbSession.get_TargetName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbc1e26aa4bf55a59b6405921d49e6b1aafa14e63a1e487caca9a7c036b1524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138318"
---
# <a name="itssbsessiontargetname-property"></a>Propiedad ITsSbSession::TargetName

Recupera el nombre del destino en el que se creó esta sesión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a una variable **BSTR** que recibe el nombre del destino en el que se creó esta sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





