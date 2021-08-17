---
description: Se llama cuando se registra una ventana como una ventana de Shell.
title: DShellWindowsEvents.WindowRegistered (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 7ad7270f9054b875eabcb1fd9f5a7ab2e299a5916d55ef4630988921b6b2f4ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455575"
---
# <a name="dshellwindowseventswindowregistered-method"></a>DShellWindowsEvents.WindowRegistered (método)

Se llama cuando se registra una ventana como una ventana de Shell.

## <a name="syntax"></a>Sintaxis


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCookie* \[ En\]
</dt> <dd>

Tipo: **Entero**

Cookie que identifica la ventana que se registró.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se concede una cookie a una ventana cuando se registra como una ventana de Shell. Para obtener más información, vea [**Registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Product<br/> | Internet Explorer 5<br/>                                                                                           |
| Archivo DLL<br/>     | <dl> <dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRevoked**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Registro**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**RegisterPending**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




