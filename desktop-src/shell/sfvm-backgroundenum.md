---
description: 'Permite que el objeto de devolución de llamada solicite la enumeración en un subproceso en segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_BACKGROUNDENUM (ShlObj. h)
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
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997828"
---
# <a name="sfvm_backgroundenum-message"></a>SFVM \_ BACKGROUNDENUM

Permite que el objeto de devolución de llamada solicite la enumeración en un subproceso en segundo plano. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>Parámetros

Este mensaje no tiene parámetros.

## <a name="remarks"></a>Observaciones

En respuesta a esta notificación, vuelva \_ a aceptar para habilitar la enumeración en segundo plano. De forma predeterminada, el objeto de la carpeta del sistema mostrará la animación "linterna" mientras se está llevando a cabo la enumeración. Para especificar una animación personalizada, controle [**SFVM \_ GETANIMATION**](sfvm-getanimation.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
