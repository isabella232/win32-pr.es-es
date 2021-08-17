---
description: SFVM \_ GETDETAILSOF puede modificarse o no estar disponible.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: SFVM_GETDETAILSOF mensaje (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6fd850a3f500a1d259ebdcae9e5c549ef76a8eab0d5e1d14c1385fbba8d27ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118048454"
---
# <a name="sfvm_getdetailsof-message"></a>Mensaje \_ GETDETAILSOF de SFVM

\[**SFVM \_ GETDETAILSOF** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible.\]

Permite que el objeto de devolución de llamada proporcione los detalles de un elemento en una carpeta de Shell. Use solo si se produce un error en una llamada a [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) y no hay ningún método [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) disponible para llamar. Usado por [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).


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
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP2<br/>                                                      |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                      |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 
