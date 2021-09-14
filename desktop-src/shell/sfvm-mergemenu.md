---
description: Permite que el objeto de devolución de llamada combine elementos de menú en los Windows explorador. Usado por IShellFolderViewCB::MessageSFVCB.
title: SFVM_MERGEMENU mensaje (Shlobj.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359666"
---
# <a name="sfvm_mergemenu-message"></a>Mensaje \_ MERGEMENU de SFVM

Permite que el objeto de devolución de llamada combine elementos de menú en los Windows explorador. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pInfo* \[ out\]
</dt> <dd>

Estructura [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) que contiene la información necesaria para combinar los elementos en el menú.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje tiene esencialmente el mismo propósito que [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) e [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) en una vista de carpeta personalizada. Consulte la *sección Using IShellBrowser to Communicate with Windows Explorer* (Uso de IShellBrowser para comunicarse con Windows Explorer) de Implementación de una vista de [carpeta](../lwef/nse-folderview.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
