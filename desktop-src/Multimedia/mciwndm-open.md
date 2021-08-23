---
title: MCIWNDM_OPEN mensaje (Vfw.h)
description: El mensaje MCIWNDM OPEN abre un dispositivo MCI y \_ lo asocia a una ventana de MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bebf9573303e3560b385425e7642106120c41456a21c1c4b80bc158328a864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428905"
---
# <a name="mciwndm_open-message"></a>Mensaje MCIWNDM \_ OPEN

El **mensaje MCIWNDM \_ OPEN** abre un dispositivo MCI y lo asocia a una ventana de MCIWnd. En el caso de los dispositivos MCI que usan archivos de datos, esta macro también puede abrir un archivo de datos especificado, nombrar un nuevo archivo que se va a crear o mostrar un cuadro de diálogo para permitir que el usuario seleccione un archivo para abrirlo. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndOpen.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Marcas asociadas al dispositivo o archivo que se abrirá. La marca MCIWNDOPENF NEW especifica que se creará un nuevo archivo con el nombre \_ especificado en **szFile**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Puntero a una cadena terminada en NULL que identifica el nombre de archivo o el nombre del dispositivo MCI que se abrirá. Especifique 1 para que este parámetro muestre el cuadro de diálogo Abrir.

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

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





