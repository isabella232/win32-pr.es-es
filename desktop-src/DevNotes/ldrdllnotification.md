---
description: Función de devolución de llamada de notificación especificada con la función LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Función de devolución de llamada LdrDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e1e9bea21cd4e21ca7549ce34343b42c50b293471e69576d7c1164f92a371c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004110"
---
# <a name="ldrdllnotification-callback-function"></a>Función de devolución de llamada LdrDllNotification

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Función de devolución de llamada de notificación especificada con [**la función LdrRegisterDllNotification.**](ldrregisterdllnotification.md) El cargador llama a esta función cuando se carga por primera vez un archivo DLL.

**Advertencia:** No es seguro que la función de devolución de llamada de notificación llame a funciones en cualquier archivo DLL.

## <a name="syntax"></a>Sintaxis


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NotificationReason* \[ En\]
</dt> <dd>

Razón por la que se llamó a la función de devolución de llamada de notificación. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                        | Significado                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ MOTIVO \_ DE NOTIFICACIÓN DE DLL \_ \_ CARGADO**</dt> <dt>1</dt> </dl>       | Se cargó el archivo DLL. El *parámetro NotificationData* apunta a una estructura DE DATOS DE **NOTIFICACIÓN CARGADA DE DLL \_ \_ \_ \_ DE LDR.** <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ MOTIVO \_ DE NOTIFICACIÓN DE DLL \_ \_ DESCARGADO**</dt> <dt>2</dt> </dl> | El archivo DLL se descargó. El *parámetro NotificationData* apunta a una estructura **DLL \_ \_ UNLOADED NOTIFICATION DATA \_ \_ de LDR.** <br/> |



 

</dd> <dt>

*NotificationData* \[ En\]
</dt> <dd>

Puntero a una constante **LDR \_ DLL \_ NOTIFICATION** union que contiene datos de notificación. Esta unión tiene la siguiente definición:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

La **estructura LDR \_ DLL LOADED \_ NOTIFICATION \_ \_ DATA** tiene la siguiente definición:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

La **estructura LDR \_ DLL \_ UNLOADED NOTIFICATION \_ \_ DATA** tiene la siguiente definición:

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

*Contexto* \[ in, opcional\]
</dt> <dd>

Puntero a datos de contexto para la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función de devolución de llamada no devuelve un valor.

## <a name="remarks"></a>Comentarios

Se llama a la función de devolución de llamada de notificación antes de que se lleve a cabo la vinculación dinámica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




