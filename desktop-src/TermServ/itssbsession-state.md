---
title: Propiedad ITsSbSession State
description: Recupera o especifica el estado de sesión.
ms.assetid: 4e769ff7-2bd5-4fcb-b2d7-4dedc853482b
ms.tgt_platform: multiple
keywords:
- Propiedad State Servicios de Escritorio remoto
- Propiedad state Servicios de Escritorio remoto , interfaz ITsSbSession
- Interfaz ITsSbSession Servicios de Escritorio remoto , propiedad State
topic_type:
- apiref
api_name:
- ITsSbSession.State
- ITsSbSession.get_State
- ITsSbSession.put_State
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d8eef2a19ff9b92f7d860bb17662e84e4028eb21a5a228819b90b0af31ba3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128175"
---
# <a name="itssbsessionstate-property"></a>Propiedad ITsSbSession::State

Recupera o especifica el estado de sesión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_State(
  [in]          TSSESSION_STATE State
);

HRESULT get_State(
  [out, retval] TSSESSION_STATE *pState
);
```



## <a name="property-value"></a>Valor de propiedad

Valor de la [**enumeración TSSESSION \_ STATE**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state) que indica el estado de una sesión.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dt>

[**ESTADO DE \_ TSSESSION**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-tssession_state)
</dt> </dl>

 

 





