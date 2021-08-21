---
description: El mensaje TAPI PHONE BUTTON se envía para notificar a la aplicación que la supervisión de la pulsación de botones está habilitada si ha detectado una pulsación de botón \_ en el teléfono local.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: PHONE_BUTTON mensaje (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec64f754725e5926a8cab1d98b25e4cb379a444bf4208d6e8f3e976dafee82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073005"
---
# <a name="phone_button-message"></a>Mensaje \_ PHONE BUTTON

El mensaje TAPI **PHONE \_ BUTTON** se envía para notificar a la aplicación que la supervisión de la pulsación de botones está habilitada si ha detectado una pulsación de botón en el teléfono local.


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

Identificador de botón o bombilla del botón que se presionó. Tenga en cuenta que los identificadores de botón de cero a 11 son siempre los botones KEYPAD, siendo "0" el identificador de botón cero, "1" el identificador de botón 1 (y así sucesivamente hasta el identificador de botón 9) y con "" como identificador de botón 10 y " " como identificador de botón \* \# 11. Hay información adicional sobre un identificador de botón disponible [**con phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) y [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Modo de botón del botón. Este parámetro usa una de las [**constantes PHONEBUTTONMODE \_**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Especifica si se trata de un evento de botón hacia abajo o un evento de botón arriba. Este parámetro usa una de las [**constantes PHONEBUTTONSTATE \_**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Se **envía un mensaje PHONE \_ BUTTON** cada vez que un botón cambia de estado. Se garantiza que, para cada evento de botón hacia abajo, se envía finalmente un evento de botón hacia arriba correspondiente. Se necesita un proveedor de servicios que no pueda detectar el botón real hacia arriba para generar el mensaje de botón hacia arriba poco después del mensaje de botón hacia abajo para cada pulsación del botón.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




