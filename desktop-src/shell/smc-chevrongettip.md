---
description: Solicita el título y el texto de un recuadro informativo de comillas angulares para el elemento especificado por la estructura SMDATA correspondiente.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Mensaje de SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985747"
---
# <a name="smc_chevrongettip-message"></a>Mensaje de CHEVRONGETTIP de SMC \_

Solicita el título y el texto de un recuadro informativo de comillas angulares para el elemento especificado por la estructura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) correspondiente.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Un puntero a un búfer que recibe una cadena Unicode terminada en **null** que contiene el título del recuadro informativo. Esta cadena no debe tener más de \_ caracteres de ruta de acceso máxima, incluido el carácter **nulo** de terminación.

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Un puntero a un búfer que recibe una cadena Unicode terminada en **null** que contiene el texto del recuadro informativo. Esta cadena no debe tener más de \_ caracteres de ruta de acceso máxima, incluido el carácter **nulo** de terminación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devolver S \_ correcto.

## <a name="remarks"></a>Observaciones

El método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) recibe esta notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Shobjidl. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl. idl</dt> </dl> |



 

 




