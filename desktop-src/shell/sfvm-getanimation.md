---
description: 'Permite que el objeto de devolución de llamada especifique que se muestre una animación mientras los elementos se enumeran en un subproceso en segundo plano. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6f8b3894-f08f-4ebf-a645-87869e7d1b20
title: Mensaje de SFVM_GETANIMATION (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60e4281689556e8315da7a9550fd69acc1a327a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156796"
---
# <a name="sfvm_getanimation-message"></a>SFVM \_ GETANIMATION

Permite que el objeto de devolución de llamada especifique que se muestre una animación mientras los elementos se enumeran en un subproceso en segundo plano. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETANIMATION 

    wParam = (WPARAM)(HINSTANCE*) phinst;

    lParam = (LPARAM)(WCHAR*) pwszName;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phinst* \[ enuncia\]
</dt> <dd>

Identificador de instancia del módulo del que se debe cargar el recurso.

</dd> <dt>

*pwszName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena Unicode terminada en null que contiene la ruta de acceso del archivo. avi o el nombre de un recurso AVI. Como alternativa, este parámetro puede constar del identificador de recurso en la palabra de orden inferior y de 0 en la palabra de orden superior. Para crear este valor, use la macro [**MAKEINTRESOURCE**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . El control carga el recurso desde el módulo especificado por HINST. Un recurso AVI debe tener el tipo "AVI".

</dd> </dl>

## <a name="remarks"></a>Observaciones

De forma predeterminada, el objeto de vista de carpeta del sistema muestra la animación de "linterna" durante una enumeración en segundo plano.

*phinst* y *pwszName* se pasarán al [control Animation](../controls/animation-control-overview.md) con un mensaje [**\_ abierto ACM**](../controls/acm-open.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
