---
title: Constantes del recopilador de eventos de Windows (Evcoll. h)
description: El SDK del recopilador de eventos de Windows contiene las siguientes constantes.
ms.assetid: 2ba862f9-6849-43b3-8914-e18ede1d63c0
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- EC_VARIANT_TYPE_MASK
- EC_VARIANT_TYPE_ARRAY
- EC_READ_ACCESS
- EC_WRITE_ACCESS
- EC_OPEN_ALWAYS
- EC_CREATE_NEW
- EC_OPEN_EXISTING
api_location:
- Evcoll.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf6e7e99186e2148bf6ec3400aadf760a79a2331
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103800956"
---
# <a name="windows-event-collector-constants"></a>Constantes del recopilador de eventos de Windows

El SDK del recopilador de eventos de Windows contiene las siguientes constantes.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**\_máscara de \_ tipo \_ variante de EC**
</dt> <dd> <dl> <dt>

0x7F
</dt> <dt>



Se usa para enmascarar el bit de la matriz desde la propiedad **Type** de una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) para extraer el tipo del valor Variant.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**\_matriz de \_ tipo \_ Variant de EC**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Cuando este bit se establece en la propiedad **Type** de una [**\_ variante EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), la variante contiene un puntero a una matriz de valores, en lugar del propio valor.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**\_acceso de lectura de EC \_**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Permiso de control de acceso de lectura que permite leer información del recopilador de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**\_acceso de escritura de EC \_**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Permiso de control de acceso de escritura que permite escribir información en el recopilador de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ abrir \_ siempre**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Abre una suscripción existente o crea la suscripción si no existe. Lo usa el método [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) .


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**\_crear \_ nuevo**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Una marca pasada a la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) que especifica que se debe crear una nueva suscripción.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ abierto \_ existente**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Una marca pasada a la función [**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) que especifica que se debe abrir una suscripción existente.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Evcoll. h</dt> </dl> |



 

 





