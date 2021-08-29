---
description: Permite que el objeto de devolución de llamada especifique un archivo de Ayuda HTML y un tema dentro de él. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_GETHELPTOPIC mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c60749b69df30e89c3ffda7a8664b901ee57f9ff0cb586f13d61abd9ca66997e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968714"
---
# <a name="sfvm_gethelptopic-message"></a>Mensaje GETHELPTOPIC de SFVM \_

Permite que el objeto de devolución de llamada especifique un archivo de Ayuda HTML y un tema dentro de él. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phtd* \[ out\]
</dt> <dd>

Dirección de una estructura [**DE DATOS \_ HELPTOPIC \_ de SFVM**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) que especifica el archivo y el tema de ayuda HTML.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
