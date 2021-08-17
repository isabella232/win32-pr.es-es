---
description: Notifica a una barra de aplicaciones cuando se abre o se cierra una aplicación de pantalla completa. Esta notificación se envía en forma de mensaje definido por la aplicación que se establece mediante el mensaje ABM \_ NEW.
title: ABN_FULLSCREENAPP mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c67ec934-088c-43e0-bff4-900d76a456e5
api_name:
- ABN_FULLSCREENAPP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 55bba51153ff90dfa69b870468a1c5002121eaccf45559821c6031aba35d4b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090795"
---
# <a name="abn_fullscreenapp-message"></a>Mensaje \_ ABN FULLSCREENAPP

Notifica a una barra de aplicaciones cuando se abre o se cierra una aplicación de pantalla completa. Esta notificación se envía en forma de mensaje definido por la aplicación que se establece mediante el [**mensaje ABM \_ NEW.**](abm-new.md)


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Fopen* 
</dt> <dd>

Marca que especifica si una aplicación de pantalla completa se está abriendo o cerrando. Este parámetro es **TRUE** si la aplicación se está abriendo o **FALSE** si se está cerrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando se abre una aplicación de pantalla completa, una barra de aplicaciones debe colocarse en la parte inferior del orden Z. Cuando se cierra, la barra de aplicaciones debe restaurar su posición de orden Z.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




