---
description: 'Permite que el objeto de devolución de llamada especifique un archivo de ayuda HTML y un tema dentro de él. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_GETHELPTOPIC (ShlObj. h)
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
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911397"
---
# <a name="sfvm_gethelptopic-message"></a>SFVM \_ GETHELPTOPIC

Permite que el objeto de devolución de llamada especifique un archivo de ayuda HTML y un tema dentro de él. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phtd* \[ enuncia\]
</dt> <dd>

Dirección de una estructura [**de \_ \_ datos de SFVM HELPTOPIC**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) que especifica el archivo de ayuda HTML y el tema.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
