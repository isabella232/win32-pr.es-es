---
description: El mensaje TAPI LINE DEVSPECIFICFEATURE se envía para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, dirección \_ o llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: LINE_DEVSPECIFICFEATURE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250142"
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

## <a name="remarks"></a>Observaciones

Un proveedor de servicios usa el mensaje **LINE \_ DEVSPECIFICFEATURE** junto con la función [**lineDevSpecificFeature.**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




