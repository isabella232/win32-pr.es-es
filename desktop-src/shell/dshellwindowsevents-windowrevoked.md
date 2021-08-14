---
description: Se llama cuando se revoca el registro de una ventana de Shell.
title: DShellWindowsEvents.WindowRevoked (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 571808962d65d25d4fb08f8d4cb57ffd1d51da67a7ba60def191edcf2fe19575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459852"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>DShellWindowsEvents.WindowRevoked (método)

Se llama cuando se revoca el registro de una ventana de Shell.

## <a name="syntax"></a>Sintaxis


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCookie* \[ En\]
</dt> <dd>

Tipo: **Entero**

Cookie que identifica la ventana que se revocó.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

A una ventana se le concede una cookie cuando se registra como una ventana de Shell. Para obtener más información, vea [**Registrar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Producto<br/> | Internet Explorer 5<br/>                                                                                           |
| Archivo DLL<br/>     | <dl> <dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Revocar**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




