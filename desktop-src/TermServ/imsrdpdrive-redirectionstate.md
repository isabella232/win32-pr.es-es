---
title: Propiedad IMsRdpDrive RedirectionState
description: Indica el estado de redireccionamiento de la unidad.
ms.assetid: 05333671-460d-4c07-8b7e-fbb7bc215353
ms.tgt_platform: multiple
keywords:
- Propiedad RedirectionState Servicios de Escritorio remoto
- Propiedad RedirectionState Servicios de Escritorio remoto , interfaz IMsRdpDrive
- Interfaz IMsRdpDrive Servicios de Escritorio remoto , propiedad RedirectionState
topic_type:
- apiref
api_name:
- IMsRdpDrive.RedirectionState
- IMsRdpDrive.get_RedirectionState
- IMsRdpDrive.put_RedirectionState
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6069ec911210fac3f4334bdf9e84da080e5536a4f4b6cfc7aca0e54fe0bd2228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118351963"
---
# <a name="imsrdpdriveredirectionstate-property"></a>IMsRdpDrive::RedirectionState, propiedad

Indica el estado de redireccionamiento de la unidad.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RedirectionState(
  [in]  VARIANT_BOOL vboolRedirState
);

HRESULT get_RedirectionState(
  [out] VARIANT_BOOL *pvboolRedirState
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **VARIANT \_ FALSE.** para deshabilitar el redireccionamiento o **VARIANT \_ TRUE**. para habilitar el redireccionamiento.

## <a name="error-codes"></a>Códigos de error

Si el método se realiza correctamente, **se devuelve S \_ OK.** Cualquier otro **valor HRESULT** indica que se ha dado error en la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID IMsRdpDrive se define como \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





