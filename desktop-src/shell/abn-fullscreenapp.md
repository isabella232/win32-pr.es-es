---
description: Notifica a una Appbar cuando una aplicación de pantalla completa se abre o se cierra. Esta notificación se envía en forma de un mensaje definido por la aplicación que se establece mediante el \_ nuevo mensaje ABN.
title: Mensaje de ABN_FULLSCREENAPP (ShellAPI. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153925"
---
# <a name="abn_fullscreenapp-message"></a>Mensaje de ABN \_ FULLSCREENAPP

Notifica a una Appbar cuando una aplicación de pantalla completa se abre o se cierra. Esta notificación se envía en forma de un mensaje definido por la aplicación que se establece mediante el [**\_ nuevo mensaje ABN**](abm-new.md) .


```C++

ABN_FULLSCREENAPP 

    fOpen = (BOOL) lParam; 

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fOpen* 
</dt> <dd>

Marca que especifica si una aplicación de pantalla completa se está abriendo o cerrando. Este parámetro es **true** si la aplicación se está abriendo o **false** si se está cerrando.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se abre una aplicación de pantalla completa, un Appbar debe colocarse en la parte inferior del orden z. Cuando se está cerrando, el control Appbar debe restaurar su posición de orden z.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




