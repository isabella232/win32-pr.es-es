---
description: El mensaje TAPI LINE REMOVE se envía para informar a una aplicación de la eliminación \_ (eliminación del sistema) de un dispositivo de línea.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: LINE_REMOVE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250052"
---
# <a name="line_remove-message"></a>MENSAJE \_ LINE REMOVE

El mensaje TAPI **LINE \_ REMOVE** se envía para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo de línea. Por lo general, esto no se usa para eliminaciones temporales, como la extracción de dispositivos PCMCIA, sino solo para eliminaciones permanentes en las que el proveedor de servicios ya no informaría del dispositivo si se reinicializaba TAPI.


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

Identificador del dispositivo de línea que se quitó.

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

## <a name="remarks"></a>Observaciones

Las aplicaciones que admiten TAPI versión 2.0 o posterior se envían un **mensaje LINE \_ REMOVE.** Esto les informa de que el dispositivo se ha quitado del sistema. El **mensaje \_ LINE REMOVE** va precedido de un mensaje LINE [**\_ CLOSE**](line-close.md) en cada identificador de línea, si la aplicación tenía abierta la línea. Este mensaje se envía a todas las aplicaciones que admiten TAPI versión 2.0 o posterior que han llamado [**a lineInitializeEx,**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)incluidas aquellas que no tienen ningún dispositivo de línea abierto en ese momento.

Las aplicaciones anteriores se envían un [**mensaje \_ LINE LINEDEVSTATE**](line-linedevstate.md) que especifica LINEDEVSTATE \_ REMOVED, seguido de un mensaje LINE \_ CLOSE. Sin embargo, a diferencia del mensaje **\_ LINE REMOVE,** estas aplicaciones anteriores solo pueden recibir estos mensajes si tienen la línea abierta cuando se quita. Si no tienen la línea abierta, su única indicación de que el dispositivo se quitó recibiría un error LINEERR NODEVICE al intentar acceder \_ al dispositivo.

Una vez quitado un dispositivo, cualquier intento de acceder al dispositivo por su identificador de dispositivo produce un \_ error LINEERR NODEVICE. Una vez que todas las aplicaciones TAPI se han apagado para que TAPI se pueda reiniciar y cuando se reinicialice TAPI, el dispositivo eliminado ya no ocupa un identificador de dispositivo.

> [!Note]  
> Implementación: es TAPI el que devuelve este LINEERR NODEVICE; después de recibir un mensaje LINE REMOVE de un proveedor de servicios; no se realizan más llamadas a ese proveedor de servicios mediante ese identificador de dispositivo de \_ línea. **\_**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ CLOSE**](line-close.md)
</dt> <dt>

[**LINE \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




