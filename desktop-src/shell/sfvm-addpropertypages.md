---
description: 'Permite que el objeto de devolución de llamada proporcione una página que se va a agregar a la hoja de propiedades propiedades del objeto seleccionado. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensaje de SFVM_ADDPROPERTYPAGES (ShlObj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997809"
---
# <a name="sfvm_addpropertypages-message"></a>SFVM \_ ADDPROPERTYPAGES

Permite que el objeto de devolución de llamada proporcione una página que se va a agregar a la hoja de propiedades **propiedades** del objeto seleccionado. Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ enuncia\]
</dt> <dd>

La dirección de una estructura de [**\_ \_ datos de SFVM PROPPAGE**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este mensaje sirve esencialmente la misma función que [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages). Vea [crear controladores de hoja de propiedades](propsheet-handlers.md) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>ShlObj. h</dt> </dl> |



 

 
