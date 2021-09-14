---
title: MCIWNDM_OPENINTERFACE mensaje (Vfw.h)
description: El mensaje MCIWNDM OPENINTERFACE adjunta el flujo de datos o el archivo asociado a la interfaz especificada \_ a una ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro MCIWndOpenInterface.
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
ms.openlocfilehash: 9c40453f4d587429508a5aae19bc432fc46088ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250821"
---
# <a name="mciwndm_openinterface-message"></a>Mensaje OPENINTERFACE de MCIWNDM \_

El **mensaje MCIWNDM \_ OPENINTERFACE** adjunta el flujo de datos o el archivo asociado a la interfaz especificada a una ventana de MCIWnd. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndOpenInterface.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)


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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface)
</dt> </dl>

 

 





