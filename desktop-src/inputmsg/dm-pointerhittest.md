---
title: DM_POINTERHITTEST mensaje
description: Se envía a una ventana, cuando se detecta por primera vez la entrada de puntero, con el fin de determinar el destino de entrada más probable para la manipulación directa.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST mensajes de entrada y notificaciones
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 23efab4606f758acfffdd02fa4c53a729f1f4a99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569149"
---
# <a name="dm_pointerhittest-message"></a>DM_POINTERHITTEST mensaje

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Se envía a una ventana, cuando se detecta por primera vez la entrada de puntero, con el fin de determinar el destino de entrada más probable para [la manipulación directa.](/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal)

> \[! Importante\]  
> Las aplicaciones de escritorio deben tener en cuenta los valores de PPP. Si la aplicación no tiene reconocimiento de PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas pueden parecer inexactas debido a la virtualización de PPP. La virtualización de PPP proporciona compatibilidad con el escalado automático a aplicaciones que no tienen reconocimiento de PPP y que están activas de forma predeterminada (los usuarios pueden desactivarla). Para obtener más información, consulte [Escritura de aplicaciones Win32 con valores altos de PPP.](/previous-versions//dd464660(v=vs.85))

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sin usar.

</dd> <dt>

*lParam* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

NULL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes](messages.md)
</dt> </dl>

 

