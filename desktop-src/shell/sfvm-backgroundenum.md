---
description: Permite que el objeto de devolución de llamada solicite la enumeración en un subproceso en segundo plano. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_BACKGROUNDENUM mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 724f971f52b57a008ec17ac316b78839a6890e3e2efee5d5a037ab4fdcd7ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592745"
---
# <a name="sfvm_backgroundenum-message"></a>Mensaje \_ BACKGROUNDENUM de SFVM

Permite que el objeto de devolución de llamada solicite la enumeración en un subproceso en segundo plano. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="remarks"></a>Comentarios

En respuesta a esta notificación, devuelva S \_ OK para habilitar la enumeración en segundo plano. De forma predeterminada, el objeto de carpeta del sistema mostrará la animación de "linterna" mientras se realiza la enumeración. Para especificar una animación personalizada, [**controle SFVM \_ GETANIMATION**](sfvm-getanimation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
