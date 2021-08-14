---
title: MCIWNDM_OPENINTERFACE mensaje (Vfw.h)
description: El mensaje MCIWNDM OPENINTERFACE asocia el flujo de datos o el archivo asociado a la interfaz especificada \_ a una ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndOpenInterface.
ms.assetid: 73cbd637-d315-4b39-a978-2b72aed1f303
keywords:
- MCIWNDM_OPENINTERFACE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPENINTERFACE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83097ad6301dbfdb4636a8478c2df8e544207df334efd27fe9695f15e0693533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373589"
---
# <a name="mciwndm_openinterface-message"></a>Mensaje OPENINTERFACE de MCIWNDM \_

El **mensaje MCIWNDM \_ OPENINTERFACE** asocia el flujo de datos o el archivo asociado a la interfaz especificada a una ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndOpenInterface.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)


```C++
MCIWNDM_OPENINTERFACE 
wParam = 0; 
lParam = (LPARAM) (LPUNKNOWN) pUnk; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="pUnk"></span><span id="punk"></span><span id="PUNK"></span>*Punk*
</dt> <dd>

Puntero a una interfaz IAVI que apunta a un archivo o a un flujo de datos de un archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si se realiza correctamente o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





