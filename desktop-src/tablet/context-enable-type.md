---
description: Indica si los mensajes de contexto se deben enviar al procedimiento de ventana de la ventana propietaria.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: Enumeración CONTEXT_ENABLE_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816830"
---
# <a name="context_enable_type-enumeration"></a>\_Enumeración de tipo de habilitación de contexto \_

Indica si los mensajes de contexto se deben enviar al procedimiento de ventana de la ventana propietaria.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**\_Habilitar contexto**
</dt> <dd>

El contexto de la tableta debe estar habilitado, lo que da lugar a que se envíen mensajes de contexto al procedimiento de ventana de la ventana propietaria.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**deshabilitar contexto \_**
</dt> <dd>

El contexto de la tableta debe estar deshabilitado, lo que impide que se envíen más mensajes de contexto al procedimiento de ventana o al receptor de eventos de la ventana propietaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITablet:: CreateContext (método)**](itablet-createcontext.md)
</dt> </dl>

 

 




