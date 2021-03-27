---
description: Se llama cuando se revoca el registro de una ventana de Shell.
title: DShellWindowsEvents. WindowRevoked, método
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
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987601"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>DShellWindowsEvents. WindowRevoked, método

Se llama cuando se revoca el registro de una ventana de Shell.

## <a name="syntax"></a>Sintaxis


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lCookie* \[ de\]
</dt> <dd>

Tipo: **Integer**

Cookie que identifica la ventana que se revocó.

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

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Revocación**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




