---
title: Mensaje de MCIWNDM_OPEN (VFW. h)
description: El \_ mensaje abierto de MCIWNDM abre un dispositivo MCI y lo asocia a una ventana de MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- Mensaje de MCIWNDM_OPEN de Windows multimedia
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
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150171"
---
# <a name="mciwndm_open-message"></a>MCIWNDM \_ abrir mensaje

El **mensaje \_ abierto de MCIWNDM** abre un dispositivo MCI y lo asocia a una ventana de MCIWnd. En el caso de los dispositivos MCI que usan archivos de datos, esta macro también puede abrir un archivo de datos especificado, asignar un nombre a un nuevo archivo que se va a crear o mostrar un cuadro de diálogo para permitir que el usuario seleccione un archivo para abrirlo. Puede enviar este mensaje explícitamente o mediante la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*
</dt> <dd>

Marcas asociadas al dispositivo o archivo que se va a abrir. La \_ nueva marca MCIWNDOPENF especifica que se creará un nuevo archivo con el nombre especificado en **szFile**.

</dd> <dt>

<span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*
</dt> <dd>

Puntero a una cadena terminada en null que identifica el nombre de archivo o dispositivo MCI que se va a abrir. Especifique 1 para este parámetro para mostrar el cuadro de diálogo Abrir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero si es correcto o un error en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





