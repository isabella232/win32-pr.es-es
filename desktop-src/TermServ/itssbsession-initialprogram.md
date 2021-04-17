---
title: Propiedad InitialProgram de ITsSbSession
description: Recupera o especifica el programa inicial para esta sesión.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad InitialProgram
- Propiedad InitialProgram Servicios de Escritorio remoto, interfaz ITsSbSession
- Servicios de Escritorio remoto de la interfaz ITsSbSession, propiedad InitialProgram
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
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490619"
---
# <a name="itssbsessioninitialprogram-property"></a>ITsSbSession:: InitialProgram (propiedad)

Recupera o especifica el programa inicial para esta sesión. El programa inicial es el programa que se inicia cuando se inicia la sesión de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


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
| IDL<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITsSbSession**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





