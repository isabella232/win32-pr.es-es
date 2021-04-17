---
title: Tipos de datos del recopilador de eventos de Windows (Evcoll. h)
description: Los tipos de datos del recopilador de eventos de Windows se usan como tipos de variables de objeto de suscripción de eventos, tipos de parámetros de función y tipos de valor devueltos de función.
ms.assetid: b78bdaf8-e034-40fe-acf8-632313e4fd94
ms.tgt_platform: multiple
keywords:
- EC_HANDLE
- EC_OBJECT_ARRAY_PROPERTY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ccec141317644aa091eac44033b87b9e4495ddc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695853"
---
# <a name="windows-event-collector-data-types"></a>Tipos de datos del recopilador de eventos de Windows

Los tipos de datos del recopilador de eventos de Windows se usan como tipos de variables de objeto de suscripción de eventos, tipos de parámetros de función y tipos de valor devueltos de función.


```C++
typedef HANDLE EC_HANDLE;
typedef HANDLE EC_OBJECT_ARRAY_PROPERTY_HANDLE;
```



<dl> <dt>

**identificador de EC \_**
</dt> <dd>

Identificador de un objeto de suscripción. Se utiliza para representar una suscripción del recopilador de eventos.

</dd> <dt>

**\_identificador de \_ propiedad de matriz de objetos de EC \_ \_**
</dt> <dd>

Identificador de una matriz de valores de propiedad para los orígenes de eventos de una suscripción. El método [**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty) devuelve el identificador de matriz cuando el valor de **EcSubscriptionEventSources** se pasa al parámetro *PropertyId* .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





