---
description: El mensaje TAPI PHONE REMOVE se envía para informar a una aplicación de la eliminación \_ (eliminación del sistema) de un dispositivo telefónico.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: PHONE_REMOVE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a26be60c55b16d0126d0b3be107a95af17dd490c9329343bb27ac6496403d46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773905"
---
# <a name="phone_remove-message"></a>Mensaje \_ PHONE REMOVE

El mensaje **TAPI PHONE \_ REMOVE** se envía para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo telefónico. Por lo general, esto no se usa para eliminaciones temporales, como la extracción de dispositivos PCMCIA, sino solo para eliminaciones permanentes en las que el proveedor de servicios ya no informaría del dispositivo si se reinicializaba TAPI.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hDevice* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador del dispositivo de teléfono que se quitó.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Reservado. Establecer en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

A las aplicaciones TAPI versión 2.0 o posterior se les envía un **mensaje PHONE \_ REMOVE.** Esto les informa de que el dispositivo se ha quitado del sistema. El **mensaje \_ PHONE REMOVE** va precedido de un mensaje PHONE [**\_ CLOSE**](phone-close.md) en cada identificador de teléfono, si la aplicación tenía el teléfono abierto. Este mensaje se envía a todas las aplicaciones que admiten TAPI versión 2.0 o posterior que han llamado [**a phoneInitializeEx,**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)incluidas aquellas que no tienen ningún dispositivo de teléfono abierto en ese momento.

Las aplicaciones anteriores (que negociaron TAPI versión 1.4 o anterior) se envían un mensaje [**PHONE \_ STATE**](phone-state.md) que especifica PHONESTATE REMOVED, seguido de un \_ mensaje PHONE [**\_ CLOSE.**](phone-close.md) Sin embargo, a diferencia del mensaje **\_ PHONE REMOVE,** estas aplicaciones anteriores solo pueden recibir estos mensajes si tienen el teléfono abierto cuando se quita. Si no tienen el teléfono abierto, su única indicación de que se quitó el dispositivo sería recibir un PHONEERR NODEVICE al intentar acceder \_ al dispositivo.

Una vez quitado un dispositivo, cualquier intento de acceder al dispositivo por su identificador de dispositivo produce un error PHONEERR \_ NODEVICE. Una vez que todas las aplicaciones TAPI se han apagado para que TAPI se pueda reiniciar y cuando se reinicialice TAPI, el dispositivo eliminado ya no ocupa un identificador de dispositivo.

> [!Note]  
> Implementación: es TAPI la que devuelve este mensaje PHONEERR NODEVICE después de recibir un mensaje PHONE REMOVE de un proveedor de servicios; no se realizan más llamadas a ese proveedor de servicios con ese identificador de dispositivo \_ \_ telefónico.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PHONE \_ CLOSE**](phone-close.md)
</dt> <dt>

[**ESTADO DEL \_ TELÉFONO**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




