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
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267772"
---
# <a name="sfvm_gethelptopic-message"></a>Mensaje \_ GETHELPTOPIC de SFVM

Permite que el objeto de devolución de llamada especifique un archivo de Ayuda HTML y un tema dentro de él. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*phtd* \[ out\]
</dt> <dd>

Dirección de una estructura [**DE DATOS \_ HELPTOPIC \_ de SFVM**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) que especifica el tema y el archivo de Ayuda HTML.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
