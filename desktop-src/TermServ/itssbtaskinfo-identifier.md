---
title: Propiedad ITsSbTaskInfo Identifier
description: Recupera un GUID que el agente de tareas usa como identificador único.
ms.assetid: 96b41588-d634-4cdd-aacc-0456b8e47c3b
ms.tgt_platform: multiple
keywords:
- Identificador de propiedad Servicios de Escritorio remoto
- Propiedad identifier Servicios de Escritorio remoto , interfaz ITsSbTaskInfo
- Interfaz ITsSbTaskInfo Servicios de Escritorio remoto , propiedad Identifier
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Identifier
- ITsSbTaskInfo.get_Identifier
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43eb5b0495b9f258f3b82df8657f104cbea0555a46f61e6a133be8f765081a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128084"
---
# <a name="itssbtaskinfoidentifier-property"></a>Propiedad ITsSbTaskInfo::Identifier

Recupera un GUID que el agente de tareas usa como identificador único.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Identifier(
  [out, retval] BSTR *pIdentifier
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor BSTR** que recibe el GUID.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





