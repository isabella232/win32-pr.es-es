---
description: Se envía el mensaje DEVSPECIFICFEATURE de línea de TAPI \_ para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 5f1a4da2-1a2a-4a18-8a69-82d27ddca9cf
title: Mensaje de LINE_DEVSPECIFICFEATURE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d45f91f4b3d45b52a345827e6535b054e9cf2c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691069"
---
# <a name="line_devspecificfeature-message"></a>Mensaje de línea \_ DEVSPECIFICFEATURE

Se envía el mensaje **\_ DEVSPECIFICFEATURE de línea** de TAPI para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de un dispositivo de línea o de una llamada a. Esto es específico del dispositivo.

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

Un proveedor de servicios usa el mensaje **line \_ DEVSPECIFICFEATURE** junto con la función [**lineDevSpecificFeature**](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature) . Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




