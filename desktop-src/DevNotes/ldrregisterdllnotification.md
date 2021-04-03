---
description: Registra la notificación cuando se carga por primera vez un archivo DLL. Esta notificación se produce antes de que tenga lugar la vinculación dinámica.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080109"
---
# <a name="ldrregisterdllnotification-function"></a>LdrRegisterDllNotification función)

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Registra la notificación cuando se carga por primera vez un archivo DLL. Esta notificación se produce antes de que tenga lugar la vinculación dinámica.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Este parámetro debe ser cero.

</dd> <dt>

*NotificationFunction* \[ de\]
</dt> <dd>

Puntero a una función de devolución de llamada de notificación [*LdrDllNotification*](ldrdllnotification.md) que se va a llamar cuando se cargue el archivo dll.

</dd> <dt>

*Contexto* \[ de en, opcional\]
</dt> <dd>

Un puntero a los datos de contexto de la función de devolución de llamada.

</dd> <dt>

*Cookie* \[ enuncia\]
</dt> <dd>

Un puntero a una variable para recibir un identificador de la función de devolución de llamada. Este identificador se usa para anular el registro de la función de devolución de llamada de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**.

Los formularios y la importancia de los códigos de error de **NTSTATUS** se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Observaciones

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK. También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[*LdrDllNotification*](ldrdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
