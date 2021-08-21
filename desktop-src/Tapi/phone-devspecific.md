---
description: TAPI envía el mensaje PHONE DEVSPECIFIC a una aplicación para notificar a la aplicación los eventos específicos del dispositivo \_ que se producen en el teléfono. El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 578ba0960963f85ff597d9a6bc87ff3369a6c837ed58367bd82d62a13341e988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072905"
---
# <a name="phone_devspecific-message"></a>MENSAJE \_ DEVSPECIFIC DE PHONE

TAPI envía el **mensaje \_ PHONE DEVSPECIFIC** a una aplicación para notificar a la aplicación los eventos específicos del dispositivo que se producen en el teléfono. El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPhone* 
</dt> <dd>

Identificador para el dispositivo de teléfono.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

La instancia de devolución de llamada de la aplicación proporcionada al abrir el dispositivo telefónico.

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
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




