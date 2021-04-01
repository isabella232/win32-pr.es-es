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
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906953"
---
# <a name="ldrdllnotification-callback-function"></a>Función de devolución de llamada LdrDllNotification

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Función de devolución de llamada de notificación especificada con la función [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) . El cargador llama a esta función cuando se carga por primera vez un archivo DLL.

**ADVERTENCIA:** No es seguro que la función de devolución de llamada de notificación llame a funciones en cualquier DLL.

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

*NotificationReason* \[ de\]
</dt> <dd>

Motivo por el que se llamó a la función de devolución de llamada de notificación. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                        | Significado                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ Motivo de notificación de DLL \_ \_ \_ cargado**</dt> <dt>1</dt> </dl>       | Se cargó el archivo DLL. El parámetro *NotificationData* apunta a una estructura de **datos de notificación de LDR \_ dll \_ cargada \_ \_** . <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ Motivo de notificación de DLL \_ \_ \_ descargado**</dt> <dt>2</dt> </dl> | El archivo DLL se ha descargado. El parámetro *NotificationData* apunta a una estructura de datos de **notificación sin \_ cargar del archivo dll \_ \_ \_ LDR** . <br/> |



 

</dd> <dt>

*NotificationData* \[ de\]
</dt> <dd>

Un puntero a una Unión **de \_ \_ notificaciones dll de LDR** de constante que contiene los datos de notificación. Esta Unión tiene la siguiente definición:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

La estructura de **datos de notificación de LDR \_ dll \_ \_ \_ cargada** tiene la siguiente definición:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

La estructura de datos de notificación de la **dll de LDR no \_ \_ cargada \_ \_** tiene la siguiente definición:

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

*Contexto* \[ de en, opcional\]
</dt> <dd>

Un puntero a los datos de contexto de la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función de devolución de llamada no devuelve un valor.

## <a name="remarks"></a>Observaciones

Se llama a la función de devolución de llamada de notificación antes de que tenga lugar la vinculación dinámica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




