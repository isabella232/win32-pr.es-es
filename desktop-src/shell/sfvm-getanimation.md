---
description: Permite que el objeto de devolución de llamada especifique que se muestre una animación mientras los elementos se enumeran en un subproceso en segundo plano. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: SFVM_GETANIMATION mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 746d8bc9bc4a6d4e15d9cd5190d7cfcb7d1362daba8ec5478b333458f62787da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008995"
---
# <a name="sfvm_getanimation-message"></a>Mensaje \_ GETANIMATION de SFVM

Permite que el objeto de devolución de llamada especifique que se muestre una animación mientras los elementos se enumeran en un subproceso en segundo plano. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phinst* \[ out\]
</dt> <dd>

Identificador de instancia del módulo desde el que se debe cargar el recurso.

</dd> <dt>

*pwszName* \[ out\]
</dt> <dd>

Puntero a una cadena Unicode terminada en NULL que contiene la ruta de acceso del archivo .avi o el nombre de un recurso AVI. Como alternativa, este parámetro puede constar del identificador de recurso en la palabra de orden bajo y 0 en la palabra de orden superior. Para crear este valor, use la [**macro MAKEINTRESOURCE.**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) El control carga el recurso desde el módulo especificado por la clase . Un recurso AVI debe tener el tipo "AVI".

</dd> </dl>

## <a name="remarks"></a>Comentarios

De forma predeterminada, el objeto de vista de carpeta del sistema muestra la animación de "linterna" durante una enumeración en segundo plano.

*phinst* y *pwszName* se pasarán al [control de animación](../controls/animation-control-overview.md) con un mensaje OPEN [**\_ de ACM.**](../controls/acm-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
