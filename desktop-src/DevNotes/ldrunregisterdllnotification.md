---
description: Cancela la notificación de carga de DLL que se registró anteriormente mediante una llamada a la función LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification función)
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
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423191"
---
# <a name="ldrunregisterdllnotification-function"></a>LdrUnregisterDllNotification función)

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Cancela la notificación de carga de DLL que se registró anteriormente mediante una llamada a la función [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cookie* \[ de\]
</dt> <dd>

Un puntero al identificador de devolución de llamada recibido de la llamada [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) que se registró para la notificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un código de error **NTSTATUS** o.

Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**.

Si no se encuentra la función de devolución de llamada, la función devuelve el **estado \_ dll \_ no \_ encontrado**.

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

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
