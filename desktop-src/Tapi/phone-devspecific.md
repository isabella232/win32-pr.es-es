---
description: TAPI envía el mensaje PHONE DEVSPECIFIC a una aplicación para notificar a la aplicación los eventos específicos del dispositivo \_ que se producen en el teléfono. El significado del mensaje y la interpretación de los parámetros están definidos por la implementación.
ms.assetid: e3e803dd-b041-48b7-9acf-a89989370204
title: PHONE_DEVSPECIFIC mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c817f273a49fdcda36995cec335811fb06c8a917
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071087"
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
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




