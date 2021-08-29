---
title: Windows Tipos de datos del recopilador de eventos (Evcoll.h)
description: Los tipos de datos del recopilador Windows eventos se usan como tipos de variables de objeto de suscripción de eventos, tipos de parámetros de función y tipos de valor devuelto de función.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8d0a3a0887fccebbd5cfb45042eaa59895febfa1001af93eed1161e9d33f8b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620575"
---
# <a name="windows-event-collector-data-types"></a>Windows Tipos de datos del recopilador de eventos

Los tipos de datos del recopilador Windows eventos se usan como tipos de variables de objeto de suscripción de eventos, tipos de parámetros de función y tipos de valor devuelto de función.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**CONTROLADOR \_ DE EC**
</dt> <dd>

Identificador de un objeto de suscripción. Se usa para representar una suscripción del recopilador de eventos.

</dd> <dt>

**IDENTIFICADOR DE \_ PROPIEDAD \_ DE LA \_ MATRIZ DE OBJETOS \_ EC**
</dt> <dd>

Controlar una matriz de valores de propiedad para los orígenes de eventos de una suscripción. El método [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) devuelve el identificador de matriz cuando el valor **EcSubscriptionEventSources** se pasa al *parámetro PropertyId.*

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Evcoll.h</dt> </dl> |



 

 





