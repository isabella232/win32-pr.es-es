---
description: SFVM \_ GETDETAILSOF puede modificarse o no estar disponible.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: SFVM_GETDETAILSOF mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361036"
---
# <a name="sfvm_getdetailsof-message"></a>Mensaje \_ GETDETAILSOF de SFVM

\[**SFVM \_ GETDETAILSOF** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada proporcione los detalles de un elemento de una carpeta shell. Use solo si se produce un error en una llamada a [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) y no hay ningún método [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) disponible para llamar a . Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iColumn* \[ En\]
</dt> <dd>

Identificador de base cero de la columna.

</dd> <dt>

*pDi* \[ out\]
</dt> <dd>

Puntero a una [**estructura DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) rellenada con la información solicitada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
