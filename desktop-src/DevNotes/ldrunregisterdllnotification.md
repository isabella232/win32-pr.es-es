---
description: Cancela la notificación de carga de DLL registrada anteriormente mediante una llamada a la función LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Función LdrUnregisterDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: c70a732f1e1d1dd71db8d89489066547ee5238e89cf992fca9f2b04759b4c9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001305"
---
# <a name="ldrunregisterdllnotification-function"></a>Función LdrUnregisterDllNotification

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Cancela la notificación de carga de DLL registrada anteriormente mediante una llamada a [**la función LdrRegisterDllNotification.**](ldrregisterdllnotification.md)

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cookie* \[ En\]
</dt> <dd>

Puntero al identificador de devolución de llamada recibido de [**la llamada LdrRegisterDllNotification**](ldrregisterdllnotification.md) que se registró para la notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **NTSTATUS o** un código de error.

Si la función se realiza correctamente, devuelve **STATUS \_ SUCCESS**.

Si no se encuentra la función de devolución de llamada, la función devuelve **STATUS \_ DLL NOT \_ \_ FOUND**.

Los formularios y la importancia de los códigos de error **NTSTATUS** se enumeran en el archivo de encabezado Ntstatus.h disponible en WDK y se describen en la documentación de WDK.

## <a name="remarks"></a>Comentarios

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, Ntdll.lib, está disponible en WDK. También puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
