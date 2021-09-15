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
ms.openlocfilehash: d73a30c9f40fc494603afd4a6cbb990f81290c8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468308"
---
# <a name="abn_fullscreenapp-message"></a>Mensaje \_ DE ABN FULLSCREENAPP

Notifica a una barra de aplicaciones cuando se abre o se cierra una aplicación de pantalla completa. Esta notificación se envía en forma de mensaje definido por la aplicación que se establece mediante el [**mensaje ABM \_ NEW.**](abm-new.md)


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Fopen* 
</dt> <dd>

Marca que especifica si una aplicación de pantalla completa se está abriendo o cerrando. Este parámetro es **TRUE** si la aplicación se abre o **FALSE** si se está cerrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se abre una aplicación de pantalla completa, una barra de aplicaciones debe colocarse en la parte inferior del orden Z. Cuando se cierra, la barra de aplicaciones debe restaurar su posición de orden Z.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




