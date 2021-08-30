---
title: Propiedad ITsSbSession InitialProgram
description: Recupera o especifica el programa inicial para esta sesión.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Propiedad InitialProgram Servicios de Escritorio remoto
- Propiedad InitialProgram Servicios de Escritorio remoto , interfaz ITsSbSession
- Interfaz ITsSbSession Servicios de Escritorio remoto , propiedad InitialProgram
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc1ec332283c6eb68d915c7fa0aa92070af1fb34f572d7a27adb058fa40de433
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989895"
---
# <a name="itssbsessioninitialprogram-property"></a>Propiedad ITsSbSession::InitialProgram

Recupera o especifica el programa inicial para esta sesión. El programa inicial es el programa que se inicia cuando se inicia la sesión de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a>Valor de propiedad

Variable **BSTR** que contiene el programa inicial.

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

 

 





