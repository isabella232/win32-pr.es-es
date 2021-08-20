---
title: BG_ERROR_CONTEXT enumeración (Deliveryoptimization.h)
description: La BG_ERROR_CONTEXT enumeración define los valores constantes que especifican el contexto en el que se produjo el error.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- BG_ERROR_CONTEXT enumeración
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffdd164589fc35d01b34aa6935e78ec39488ce41cfefc044baaa5048670f730f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914725"
---
# <a name="bg_error_context-enumeration"></a>BG_ERROR_CONTEXT enumeración

La **BG_ERROR_CONTEXT** enumeración define los valores constantes que especifican el contexto en el que se produjo el error.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**
</dt> <dd>

No se ha producido un error.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**
</dt> <dd>

El error estaba relacionado con el archivo remoto especificado. Por ejemplo, la dirección URL no era accesible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**
</dt> <dd>

No compatible.

</dd> <dt>

<span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**
</dt> <dd>

No compatible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





