---
description: 'Permite que el objeto de devolución de llamada proporcione información de zona de Internet. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6fae7925-b1be-4270-9318-7fa517563dad
title: Mensaje de SFVM_GETZONE (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5586188aeab6a054e22e4b242039beaae1ce390d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546934"
---
# <a name="sfvm_getzone-message"></a>SFVM \_ GETZONE

\[Esta notificación se admite a través de Windows XP Service Pack 2 (SP2) y Windows Server 2003. Es posible que no se admita en versiones posteriores de Windows.\]

Permite que el objeto de devolución de llamada proporcione información de zona de Internet. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETZONE
    lParam = (LPARAM)(DWORD*) zone;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*zona* \[ de enuncia\]
</dt> <dd>

Uno de los siguientes valores que indican la zona de Internet. Estos valores constituyen la enumeración [**URLZONE**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537175(v=vs.85)) , que se define en urlmon. h.

<dt>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>

<span id="URLZONE_LOCAL_MACHINE"></span><span id="urlzone_local_machine"></span>**\_máquina local \_ URLZONE**


</dt> <dd>

Zona utilizada para el contenido que ya está en el equipo local del usuario. La interfaz de usuario no expone esta zona.

</dd> <dt>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>

<span id="URLZONE_INTRANET"></span><span id="urlzone_intranet"></span>**Intranet de URLZONE \_**


</dt> <dd>

Zona utilizada para el contenido que se encuentra en una intranet.

</dd> <dt>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>

<span id="URLZONE_TRUSTED"></span><span id="urlzone_trusted"></span>**URLZONE de \_ confianza**


</dt> <dd>

Zona utilizada para sitios web de confianza en Internet.

</dd> <dt>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>

<span id="URLZONE_INTERNET"></span><span id="urlzone_internet"></span>**URLZONE \_ Internet**


</dt> <dd>

Zona utilizada para la mayor parte del contenido de Internet.

</dd> <dt>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>

<span id="URLZONE_UNTRUSTED"></span><span id="urlzone_untrusted"></span>**URLZONE que no es de \_ confianza**


</dt> <dd>

Zona usada para sitios web que no son de confianza.

</dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
