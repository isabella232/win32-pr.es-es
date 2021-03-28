---
description: 'Permite que el objeto de devolución de llamada Combine los elementos de menú en los menús del explorador de Windows. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_MERGEMENU (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986075"
---
# <a name="sfvm_mergemenu-message"></a>SFVM \_ MERGEMENU

Permite que el objeto de devolución de llamada Combine los elementos de menú en los menús del explorador de Windows. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pinfo* \[ enuncia\]
</dt> <dd>

Estructura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contiene la información necesaria para combinar los elementos en el menú.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje sirve esencialmente el mismo propósito que [**IShellBrowser:: InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) y [**IShellBrowser:: SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) en una vista de carpeta personalizada. Vea la sección *uso de IShellBrowser para comunicarse con el explorador de Windows* de implementación de [una vista de carpeta](../lwef/nse-folderview.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
