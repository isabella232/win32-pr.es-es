---
description: TAPI envía el mensaje PHONE \_ STATE a una aplicación cada vez que cambia el estado de un dispositivo de teléfono.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: PHONE_STATE mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90003eaa67cb3384b123c62827fcf52bae524b1e20f9f14c2391c46dc89a367c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796765"
---
# <a name="phone_state-message"></a>Mensaje \_ DE ESTADO DEL TELÉFONO

TAPI envía el mensaje **PHONE \_ STATE** a una aplicación cada vez que cambia el estado de un dispositivo de teléfono.


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

Estado del teléfono que ha cambiado. Este parámetro usa una de las [**constantes PHONESTATE \_**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Teléfono información dependiente del estado que detalla el cambio de estado. Este parámetro no se usa si se establecen varias marcas en *dwParam1*, porque han cambiado varios elementos de estado. La aplicación debe invocar [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) para obtener un conjunto completo de información.

Si *dwParam1* es PHONESTATE \_ OWNER, *dwParam2* contiene el nuevo número de propietarios.

Si *dwParam1* es PHONESTATE \_ MONITORS, *dwParam2* contiene el nuevo número de monitores.

Si *dwParam1* es PHONESTATE \_ LAMP, *dwParam2* contiene el identificador de botón o bombilla de la bombilla que ha cambiado.

Si *dwParam1* es PHONESTATE \_ RINGMODE, *dwParam2* contiene el nuevo modo de anillo.

Si *dwParam1* es PHONESTATE \_ HANDSET, SPEAKER o HEADSET, *dwParam2* contiene el nuevo modo hookswitch de ese dispositivo de conmutador de enlace. Este parámetro usa una de las [**constantes PHONEHOOKSWITCHMODE \_**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El envío **del \_ mensaje PHONE STATE** a la aplicación se puede controlar y consultar mediante [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) y [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). De forma predeterminada, este mensaje está deshabilitado para todos los cambios de estado excepto para PHONESTATE \_ REINIT, que no se puede deshabilitar. Este mensaje se envía a todas las aplicaciones que tienen un identificador al teléfono, incluidas las que llamaron [**a phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con el parámetro *dwPrivileges* establecido en PHONEPRIVILEGE OWNER o \_ PHONEPRIVILEGE \_ MONITOR.

Se **envía un mensaje DE \_ ESTADO** DE TELÉFONO con una indicación de propietarios o monitores a las aplicaciones que ya tienen un identificador para el teléfono. Esto puede ser el resultado de que otra aplicación cambie la propiedad o la supervisión del dispositivo telefónico con [**phoneOpen,**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) o [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PHONE \_ CLOSE**](phone-close.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




