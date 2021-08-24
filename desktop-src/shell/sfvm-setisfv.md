---
description: Notifica al objeto de devolución de llamada del sitio del contenedor. Solo se usa cuando no se admite IObjectWithSite::SetSite y se usa SHCreateShellFolderViewEx. Usado por IShellFolderViewCB::MessageSFVCB.
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: SFVM_SETISFV mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e6d9ad3e9b1b8302089da8a59a8d5502a04392da77c6fc5276725b144efa026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660805"
---
# <a name="sfvm_setisfv-message"></a>Mensaje \_ DE SFVM SETISFV

\[Esta notificación se admite a través Windows XP Service Pack 2 (SP2) y Windows Server 2003. Es posible que no se pueda usar en versiones posteriores de Windows.\]

Notifica al objeto de devolución de llamada del sitio del contenedor. Solo se usa cuando no se admite [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) y [**se usa SHCreateShellFolderViewEx.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sitio* \[ En\]
</dt> <dd>

Puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sitio de contenedor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
