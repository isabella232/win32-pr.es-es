---
description: Se envía el mensaje de eliminación de línea TAPI \_ para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo de línea.
ms.assetid: 21b912d6-34aa-4ac0-b019-be3c851cc96d
title: Mensaje de LINE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567ead3ad2941845dd22405f0d8706eca74bfbd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680364"
---
# <a name="line_remove-message"></a>Mensaje de eliminación de línea \_

Se envía el mensaje de eliminación de **línea \_** TAPI para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo de línea. Por lo general, esto no se utiliza para las eliminaciones temporales, como la extracción de dispositivos PCMCIA, sino solo para las eliminaciones permanentes en las que el proveedor de servicios ya no debe informar del dispositivo si se reinicializara TAPI.


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

Identificador del dispositivo de línea que se ha quitado.

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

Las aplicaciones que admiten la versión 2,0 o posterior de TAPI recibirán un mensaje de **\_ eliminación de línea** . Esto les informa de que el dispositivo se ha quitado del sistema. El mensaje de **\_ eliminación de línea** está precedido por un mensaje de [**\_ cierre de línea**](line-close.md) en cada identificador de línea, si la aplicación tenía abierta la línea. Este mensaje se envía a todas las aplicaciones que admiten la versión 2,0 o posterior de TAPI que han llamado a [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa), incluidos los que no tienen dispositivos de línea abiertos en este momento.

A las aplicaciones anteriores se les envía un mensaje de [**línea \_ LINEDEVSTATE**](line-linedevstate.md) que especifica LINEDEVSTATE \_ quitado, seguido de un mensaje de cierre de línea \_ . Sin embargo, a diferencia del mensaje de **\_ eliminación de línea** , estas aplicaciones antiguas solo pueden recibir estos mensajes si tienen la línea abierta cuando se quita. Si no tienen abierta la línea, su única indicación de que el dispositivo se ha quitado recibirá un \_ error LINEERR Device al intentar acceder al dispositivo.

Una vez que se ha quitado un dispositivo, cualquier intento de acceder al dispositivo por su identificador de dispositivo produce un \_ error LINEERR Device. Una vez que se han cerrado todas las aplicaciones TAPI para que TAPI pueda reiniciarse y, cuando se reinicialice TAPI, el dispositivo que se ha quitado ya no ocupa un identificador de dispositivo.

> [!Note]  
> Implementación: es TAPI que devuelve este LINEERR \_ Device; una vez que se recibe un mensaje de **\_ eliminación de línea** de un proveedor de servicios; no se realizan más llamadas a ese proveedor de servicios con ese identificador de dispositivo de línea.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**cierre de línea \_**](line-close.md)
</dt> <dt>

[**LÍNEA \_ LINEDEVSTATE**](line-linedevstate.md)
</dt> <dt>

[**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa)
</dt> </dl>

 

 




