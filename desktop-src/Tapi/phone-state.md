---
description: TAPI envía el \_ mensaje de estado de teléfono a una aplicación cada vez que cambia el estado de un dispositivo de teléfono.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Mensaje de PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678905"
---
# <a name="phone_state-message"></a>Mensaje de estado de teléfono \_

TAPI envía el mensaje de **\_ Estado de teléfono** a una aplicación cada vez que cambia el estado de un dispositivo de teléfono.


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

Estado del teléfono que ha cambiado. Este parámetro utiliza una de las [**\_ constantes de PHONESTATE**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Información dependiente del estado del teléfono que detalla el cambio de estado. Este parámetro no se utiliza si se establecen varias marcas en *dwParam1*, porque han cambiado varios elementos de estado. La aplicación debe invocar [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) para obtener un conjunto de información completo.

Si *dwParam1* es PHONESTATE \_ Owner, *dwParam2* contiene el nuevo número de propietarios.

Si *dwParam1* es PHONESTATE \_ supervisa, *dwParam2* contiene el nuevo número de monitores.

Si *dwParam1* es PHONESTATE \_ LAMP, *dwParam2* contiene el identificador de botón o lámpara de la lámpara que ha cambiado.

Si *dwParam1* es PHONESTATE \_ RINGMODE, *dwParam2* contiene el nuevo modo de anillo.

Si *dwParam1* es PHONESTATE \_ auricular, altavoces o auriculares, *dwParam2* contiene el nuevo modo conmutador de ese dispositivo conmutador. Este parámetro utiliza una de las [**\_ constantes de PHONEHOOKSWITCHMODE**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El envío del mensaje de **\_ Estado telefónico** a la aplicación se puede controlar y consultar mediante [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) y [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). De forma predeterminada, este mensaje está deshabilitado para todos los cambios de estado excepto PHONESTATE \_ reinit, que no se puede deshabilitar. Este mensaje se envía a todas las aplicaciones que tienen un identificador al teléfono, incluidos los que llaman a [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) con el parámetro *DWPRIVILEGES* establecido en PHONEPRIVILEGE \_ Owner o \_ PHONEPRIVILEGE monitor.

Se envía un mensaje de **\_ Estado de teléfono** con una indicación de propietarios y/o monitores a las aplicaciones que ya tienen un identificador para el teléfono. Esto puede ser el resultado de que otra aplicación cambie la propiedad o supervise el dispositivo telefónico con [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) o [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_cerrar teléfono**](phone-close.md)
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

 

 




