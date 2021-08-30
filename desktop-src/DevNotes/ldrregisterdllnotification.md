---
description: Se registra para la notificación cuando se carga por primera vez un archivo DLL. Esta notificación se produce antes de que se produzca la vinculación dinámica.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Función LdrRegisterDllNotification
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
ms.openlocfilehash: a71798459f487724705b25db019a1f20d77f87ad5a2e4173b47282db062508ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079805"
---
# <a name="ldrregisterdllnotification-function"></a>Función LdrRegisterDllNotification

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Se registra para la notificación cuando se carga por primera vez un archivo DLL. Esta notificación se produce antes de que se produzca la vinculación dinámica.

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

*Marcas* \[ En\]
</dt> <dd>

Este parámetro debe ser cero.

</dd> <dt>

*NotificationFunction* \[ En\]
</dt> <dd>

Puntero a una función de devolución de llamada de notificación [*LdrDllNotification*](ldrdllnotification.md) a la que llamar cuando se carga el archivo DLL.

</dd> <dt>

*Contexto* \[ en, opcional\]
</dt> <dd>

Puntero a los datos de contexto de la función de devolución de llamada.

</dd> <dt>

*Cookie* \[ out\]
</dt> <dd>

Puntero a una variable para recibir un identificador para la función de devolución de llamada. Este identificador se usa para anular el registro de la función de devolución de llamada de notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve **STATUS \_ SUCCESS**.

Los formatos y la importancia de los códigos de error **NTSTATUS** se enumeran en el archivo de encabezado Ntstatus.h disponible en WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Comentarios

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, Ntdll.lib, está disponible en WDK. También puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[*LdrDllNotification*](ldrdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
