---
description: Se envía el mensaje DEVSPECIFICEX de línea de TAPI \_ para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.
ms.assetid: 137e91fd-a09e-430c-9d46-8e5be65f03d1
title: Mensaje de LINE_DEVSPECIFICEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba25047858c641ea4c6cec7d15ba06df24e8ee39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680626"
---
# <a name="line_devspecificex-message"></a>Mensaje de línea \_ DEVSPECIFICEX

Se envía el mensaje **\_ DEVSPECIFICEX de línea** de TAPI para notificar a la aplicación los eventos específicos del dispositivo que se producen en una línea, una dirección o una llamada. El significado del mensaje y la interpretación de los parámetros son específicos del dispositivo.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Identificador de un dispositivo de línea o de una llamada a. Este parámetro es específico del dispositivo.

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

Un proveedor de servicios usa el mensaje **line \_ DEVSPECIFICEX** junto con la función [**lineDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-linedevspecific) . Su significado es específico del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,2<br/>                                                      |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




