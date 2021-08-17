---
title: Propiedad ITsSbTaskInfo Label
description: Recupera la etiqueta que describe el propósito de la tarea.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Etiqueta de propiedad Servicios de Escritorio remoto
- Propiedad Label Servicios de Escritorio remoto , interfaz ITsSbTaskInfo
- Interfaz ITsSbTaskInfo Servicios de Escritorio remoto , propiedad Label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e2414dd83d44add4084a4176f575817875e933f9770039e49b02364bd8103cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138308"
---
# <a name="itssbtaskinfolabel-property"></a>Propiedad ITsSbTaskInfo::Label

Recupera la etiqueta que describe el propósito de la tarea.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor BSTR** que contiene la etiqueta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





