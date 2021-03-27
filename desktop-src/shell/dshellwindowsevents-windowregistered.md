---
description: Se llama cuando una ventana se registra como una ventana de Shell.
title: DShellWindowsEvents. WindowRegistered, método
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
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987589"
---
# <a name="dshellwindowseventswindowregistered-method"></a>DShellWindowsEvents. WindowRegistered, método

Se llama cuando una ventana se registra como una ventana de Shell.

## <a name="syntax"></a>Sintaxis


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCookie* \[ de\]
</dt> <dd>

Tipo: **Integer**

Cookie que identifica la ventana que se registró.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se concede una cookie a una ventana cuando se registra como una ventana de Shell. Para obtener más información, consulte [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Producto<br/> | Internet Explorer 5<br/>                                                                                           |
| Archivo DLL<br/>     | <dl> <dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRevoked**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Registrarse**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**RegisterPending**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




