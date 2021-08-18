---
description: Solicita el título y el texto de una información de contenido adicional para el elemento especificado por la estructura SMDATA adjunta.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: SMC_CHEVRONGETTIP mensaje (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968244"
---
# <a name="smc_chevrongettip-message"></a>Mensaje \_ SMC CHEVRONGETTIP

Solicita el título y el texto de una información de contenido adicional para el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) adjunta.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Puntero a un búfer que recibe una cadena Unicode terminada en **NULL** que contiene el título de la información. Esta cadena no debe tener más de max \_ path de longitud, incluido el carácter **NULL final.**

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Puntero a un búfer que recibe una cadena Unicode terminada en **NULL** que contiene el texto de la información. Esta cadena no debe tener más de max \_ path de longitud, incluido el carácter **NULL final.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

El método [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




