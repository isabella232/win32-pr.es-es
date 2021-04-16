---
description: Se envía el mensaje de eliminación del teléfono TAPI \_ para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo telefónico.
ms.assetid: 7c888976-65da-477a-b5a6-6e78d5f603b1
title: Mensaje de PHONE_REMOVE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab32ba8b8a8e003c5d87109dd2d0c9dbe98c236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690400"
---
# <a name="phone_remove-message"></a>TELÉFONO- \_ quitar mensaje

Se envía el mensaje de eliminación del **teléfono \_** TAPI para informar a una aplicación de la eliminación (eliminación del sistema) de un dispositivo telefónico. Por lo general, esto no se utiliza para las eliminaciones temporales, como la extracción de dispositivos PCMCIA, sino solo para las eliminaciones permanentes en las que el proveedor de servicios ya no debe informar del dispositivo si se reinicializara TAPI.


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

Identificador del dispositivo telefónico que se ha quitado.

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

Las aplicaciones TAPI versión 2,0 o posterior se envían un mensaje para **\_ quitar un teléfono** . Esto les informa de que el dispositivo se ha quitado del sistema. El mensaje para **\_ quitar el teléfono** está precedido por un mensaje de [**\_ cierre**](phone-close.md) de teléfono en cada identificador de teléfono, si la aplicación tenía el teléfono abierto. Este mensaje se envía a todas las aplicaciones que admiten la versión 2,0 o posterior de TAPI que han llamado a [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa), incluidos los que no tienen dispositivos de teléfono abiertos en este momento.

A las aplicaciones anteriores (que negociaron la versión 1,4 o anterior de TAPI) se les envía un mensaje de [**\_ Estado de teléfono**](phone-state.md) que especifica PHONESTATE \_ quitado, seguido de un mensaje de [**\_ cierre de teléfono**](phone-close.md) . Sin embargo, a diferencia del mensaje para **\_ quitar el teléfono** , estas aplicaciones antiguas solo pueden recibir estos mensajes si tienen el teléfono abierto cuando se quita. Si no tienen el teléfono abierto, su única indicación de que el dispositivo se ha quitado recibirá un PHONEERR \_ Device cuando intente obtener acceso al dispositivo.

Una vez que se ha quitado un dispositivo, cualquier intento de acceder al dispositivo por su identificador de dispositivo produce un \_ error PHONEERR Device. Una vez que se han cerrado todas las aplicaciones TAPI para que TAPI pueda reiniciarse y, cuando se reinicialice TAPI, el dispositivo que se ha quitado ya no ocupa un identificador de dispositivo.

> [!Note]  
> Implementación: es TAPI que devuelve este \_ mensaje de PHONEERR Device después \_ de recibir un mensaje de eliminación de teléfono de un proveedor de servicios; no se realizan más llamadas a ese proveedor de servicios con ese identificador de dispositivo de teléfono.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_cerrar teléfono**](phone-close.md)
</dt> <dt>

[**Estado del teléfono \_**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




