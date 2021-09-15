---
description: Las funciones prototipo del controlador de eventos se usan para todas las funciones que controlan los eventos de notificación de Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Función de devolución de llamada Prototipo de función de controlador de eventos
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271439"
---
# <a name="event-handler-function-prototype-callback-function"></a>Función de devolución de llamada Prototipo de función de controlador de eventos

\[Las funciones prototipo del controlador de eventos ya no están disponibles para su uso a partir de Windows Server 2008 y Windows Vista. \]

Las funciones prototipo del controlador de eventos se usan para todas las funciones que controlan los eventos de notificación de [*Winlogon.*](/windows/desktop/SecGloss/w-gly) El nombre de la función, representado a continuación por el nombre de la función del controlador de eventos del titular de la posición , normalmente refleja el nombre del evento que controla la función. *\_ \_ \_* Por ejemplo, la función que controla los eventos de inicio de sesión podría denominarse: **WLEventLogon**.

## <a name="syntax"></a>Sintaxis


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [**DE INFORMACIÓN DE NOTIFICACIÓN \_ DE \_ WLX**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) que contiene los detalles del evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función de devolución de llamada no devuelve un valor.

## <a name="remarks"></a>Observaciones

Si el controlador de eventos necesita crear procesos secundarios, debe llamar a la [**función CreateProcessAsUser.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) De lo contrario, el nuevo proceso se creará en el escritorio de Winlogon, no en el escritorio del usuario.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo implementar controladores de eventos para eventos winlogon. Para simplificar, solo se muestran las implementaciones de los controladores de eventos Logon y Logoff. Puede implementar controladores para el resto de los eventos exactamente de la misma manera.


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



 

