---
description: Permite que el objeto de devolución de llamada agregue botones a la barra de herramientas. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_GETBUTTONINFO mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361037"
---
# <a name="sfvm_getbuttoninfo-message"></a>Mensaje \_ GETBUTTONINFO de SFVM

Permite que el objeto de devolución de llamada agregue botones a la barra de herramientas. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ptbinfo* \[ out\]
</dt> <dd>

Dirección de una estructura [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) que especifica el número de botones y cómo se van a agregar a la barra de herramientas.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los botones se pueden anexar o anteponer a los botones de objeto de vista de carpetas del sistema estándar o mostrarse en lugar de los botones estándar. Este mensaje va seguido de un [**mensaje \_ GETBUTTONS**](sfvm-getbuttons.md) de SFVM que recupera la información relativa a los detalles del botón.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
