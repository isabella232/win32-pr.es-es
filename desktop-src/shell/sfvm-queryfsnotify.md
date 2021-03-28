---
description: SFVM \_ QUERYFSNOTIFY puede modificarse o no estar disponible.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Mensaje de SFVM_QUERYFSNOTIFY (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279392"
---
# <a name="sfvm_queryfsnotify-message"></a>SFVM \_ QUERYFSNOTIFY

\[**SFVM \_ QUERYFSNOTIFY** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada registre una carpeta para que los cambios en la vista de esa carpeta generen notificaciones. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*shcne* \[ in, out\]
</dt> <dd>

Estructura que contiene el PIDL del elemento que se va a inspeccionar en busca de eventos y una indicación de si también se deben inspeccionar las subcarpetas de ese elemento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
