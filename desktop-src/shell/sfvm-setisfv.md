---
description: 'Notifica el objeto de devolución de llamada del sitio del contenedor. Solo se usa cuando no se admite IObjectWithSite:: SetSite y se usa SHCreateShellFolderViewEx. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Mensaje de SFVM_SETISFV (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986099"
---
# <a name="sfvm_setisfv-message"></a>SFVM \_ SETISFV

\[Esta notificación se admite a través de Windows XP Service Pack 2 (SP2) y Windows Server 2003. Es posible que no se admita en versiones posteriores de Windows.\]

Notifica el objeto de devolución de llamada del sitio del contenedor. Solo se usa cuando no se admite [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) y se usa [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) . Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sitio* \[ de de\]
</dt> <dd>

Puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sitio del contenedor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
