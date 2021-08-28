---
description: El mensaje TAPI LINE DEVSPECIFICFEATURE se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, dirección \_ o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: LINE_DEVSPECIFICFEATURE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c1ec56a41d6e57c6e090c9af682cb91c8ffdb891e376fcd9760ff1b51c5d51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012535"
---
# <a name="line_devspecificfeature-message"></a>Mensaje \_ LINE DEVSPECIFICFEATURE

El mensaje TAPI **LINE \_ DEVSPECIFICFEATURE** se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, dirección o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Un identificador para un dispositivo de línea o una llamada. Esto es específico del dispositivo.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada proporcionada al abrir la línea.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Específico del dispositivo.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Específico del dispositivo.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Específico del dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Un proveedor de servicios usa el mensaje **LINE \_ DEVSPECIFICFEATURE** junto con la función [**lineDevSpecificFeature.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




