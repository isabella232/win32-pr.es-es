---
description: TAPI envía el \_ mensaje Phone DEVSPECIFIC a una aplicación para notificar a la aplicación los eventos específicos del dispositivo que se producen en el teléfono. El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: Mensaje de PHONE_DEVSPECIFIC (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678906"
---
# <a name="phone_devspecific-message"></a>Mensaje de teléfono \_ DEVSPECIFIC

TAPI envía el mensaje **Phone \_ DEVSPECIFIC** a una aplicación para notificar a la aplicación los eventos específicos del dispositivo que se producen en el teléfono. El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Identificador del dispositivo telefónico.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instancia de devolución de llamada de la aplicación que se proporciona al abrir el dispositivo telefónico.

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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




