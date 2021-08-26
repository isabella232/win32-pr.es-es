---
title: Windows Constantes del recopilador de eventos (Evcoll.h)
description: El SDK Windows Recopilador de eventos contiene las siguientes constantes.
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
ms.openlocfilehash: 8d168ecb16c293c524c4dffcb16aee7db2924e23219e42d402939ab26b4bbecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005985"
---
# <a name="windows-event-collector-constants"></a>Windows Constantes del recopilador de eventos

El SDK Windows Recopilador de eventos contiene las siguientes constantes.

<dl> <dt>

<span id="EC_VARIANT_TYPE_MASK"></span><span id="ec_variant_type_mask"></span>**EC \_ VARIANT \_ TYPE \_ MASK**
</dt> <dd> <dl> <dt>

0x7f
</dt> <dt>



Se usa para enmascarar el bit de matriz de **la propiedad Type** de una VARIANTE [**\_ DE EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant) para extraer el tipo del valor de variante.


</dt> </dl> </dd> <dt>

<span id="EC_VARIANT_TYPE_ARRAY"></span><span id="ec_variant_type_array"></span>**EC \_ VARIANT \_ TYPE \_ ARRAY**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Cuando este bit se establece en la propiedad **Type** de una VARIANTE [**\_ DE EC**](/windows/desktop/api/Evcoll/ns-evcoll-ec_variant), la variante contiene un puntero a una matriz de valores, en lugar del propio valor.


</dt> </dl> </dd> <dt>

<span id="EC_READ_ACCESS"></span><span id="ec_read_access"></span>**ACCESO \_ DE LECTURA DE \_ EC**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Permiso de control de acceso de lectura que permite leer información del recopilador de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_WRITE_ACCESS"></span><span id="ec_write_access"></span>**ACCESO \_ DE ESCRITURA DE \_ EC**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Permiso de control de acceso de escritura que permite escribir información en el recopilador de eventos.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_ALWAYS"></span><span id="ec_open_always"></span>**EC \_ OPEN \_ ALWAYS**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Abre una suscripción existente o crea la suscripción si no existe. Usado por [**el método EcOpenSubscription.**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)


</dt> </dl> </dd> <dt>

<span id="EC_CREATE_NEW"></span><span id="ec_create_new"></span>**EC \_ CREATE \_ NEW**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Marca que se pasa a [**la función EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) y que especifica que se debe crear una nueva suscripción.


</dt> </dl> </dd> <dt>

<span id="EC_OPEN_EXISTING"></span><span id="ec_open_existing"></span>**EC \_ OPEN \_ EXISTING**
</dt> <dd> <dl> <dt>

2
</dt> <dt>



Marca que se pasa a [**la función EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription) y que especifica que se debe abrir una suscripción existente.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                      |
| Header<br/>                   | <dl> <dt>Evcoll.h</dt> </dl> |



 

 





