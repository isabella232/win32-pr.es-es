---
title: Propiedad TargetName de ITsSbSession
description: Recupera el nombre del destino en el que se creó esta sesión.
ms.assetid: 5ab4cdd6-9f5f-4253-9b80-6cc35cff8b79
ms.tgt_platform: multiple
keywords:
- Propiedad TargetName Servicios de Escritorio remoto
- Propiedad TargetName Servicios de Escritorio remoto, interfaz ITsSbSession
- Servicios de Escritorio remoto de la interfaz ITsSbSession, propiedad TargetName
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
ms.openlocfilehash: dc703a32faedd250115da0b95215e620a8c15e19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686206"
---
# <a name="itssbsessiontargetname-property"></a>ITsSbSession:: TargetName (propiedad)

Recupera el nombre del destino en el que se creó esta sesión.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TargetName(
  [out, retval] BSTR *targetName
);
```



## <a name="property-value"></a>Valor de propiedad

Un puntero a una variable **BSTR** que recibe el nombre del destino en el que se creó esta sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





