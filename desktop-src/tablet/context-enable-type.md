---
description: Indica si se deben enviar mensajes de contexto al procedimiento de ventana de la ventana propietaria.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE enumeración
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360338"
---
# <a name="context_enable_type-enumeration"></a>ENUMERACIÓN CONTEXT \_ ENABLE \_ TYPE

Indica si se deben enviar mensajes de contexto al procedimiento de ventana de la ventana propietaria.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT \_ ENABLE**
</dt> <dd>

El contexto de la tableta debe estar habilitado, lo que da lugar a que se envíen mensajes de contexto al procedimiento de ventana de la ventana propietaria.

</dd> <dt>

<span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**DESHABILITACIÓN DE \_ CONTEXTO**
</dt> <dd>

El contexto de la tableta debe deshabilitarse, lo que impide que se envíen más mensajes de contexto al procedimiento de ventana o al receptor de eventos de la ventana propietaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITablet::CreateContext (Método)**](itablet-createcontext.md)
</dt> </dl>

 

 




