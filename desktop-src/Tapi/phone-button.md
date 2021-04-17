---
description: Se envía el mensaje del botón del teléfono TAPI \_ para notificar a la aplicación que la supervisión de la pulsación de botones está habilitada si ha detectado una pulsación de botón en el teléfono local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: Mensaje de PHONE_BUTTON (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680427"
---
# <a name="phone_button-message"></a>Mensaje de botón de teléfono \_

Se envía el mensaje del **\_ botón del teléfono** TAPI para notificar a la aplicación que la supervisión de la pulsación de botones está habilitada si ha detectado una pulsación de botón en el teléfono local.


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

El identificador de botón o lámpara del botón que se presionó. Tenga en cuenta que los identificadores de botón del 0 al 11 siempre son los botones del teclado, donde "0" es el identificador de botón cero, "1" es el identificador de botón 1 (y así sucesivamente hasta el identificador de botón 9) y "" es el identificador de \* botón 10, y " \# " es el identificador de botón 11. La información adicional sobre un identificador de botón está disponible con [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modo de botón del botón. Este parámetro utiliza una de las [**\_ constantes de PHONEBUTTONMODE**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Especifica si se trata de un evento de botón o un evento de botón. Este parámetro utiliza una de las [**\_ constantes de PHONEBUTTONSTATE**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Se envía un mensaje de **\_ botón de teléfono** cada vez que un botón cambia de estado. Se garantiza que una aplicación para cada evento de presionar el botón, se envía un evento Button up correspondiente. Un proveedor de servicios que no es capaz de detectar el botón real es necesario para generar el mensaje de botón arriba justo después del mensaje de botón abajo para cada pulsación de botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




