---
title: Mensaje de WM_CAP_FILE_SAVEAS (VFW. h)
description: El \_ \_ \_ mensaje de almacenamiento Cap de WM copia el contenido del archivo de captura en otro archivo. Puede enviar este mensaje explícitamente o mediante la macro capFileSaveAs.
ms.assetid: fab37bee-3160-4ebc-b58f-46021ed49b55
keywords:
- Mensaje de WM_CAP_FILE_SAVEAS de Windows multimedia
topic_type:
- apiref
api_name:
- WM_CAP_FILE_SAVEAS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aca099fefab7ca0f4ef391b1b65e89938a947a01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422113"
---
# <a name="wm_cap_file_saveas-message"></a>\_ \_ Mensaje SaveAs de archivo Cap de WM \_

El mensaje de **\_ \_ \_ almacenamiento Cap de WM** copia el contenido del archivo de captura en otro archivo. Puede enviar este mensaje explícitamente o mediante la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) .


```C++
WM_CAP_FILE_SAVEAS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Puntero a la cadena terminada en null que contiene el nombre del archivo de destino que se usa para copiar el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto o **false** en caso contrario.

Si se produce un error y se establece una función de devolución de llamada de error con el mensaje de [**\_ error de devolución de \_ \_ llamada \_ de Cap de WM**](wm-cap-set-callback-error.md) , se llama a la función de devolución de llamada de error.

## <a name="remarks"></a>Observaciones

Este mensaje no cambia el nombre o el contenido del archivo de captura actual.

Si la operación de copia no se realiza correctamente debido a un error de disco lleno, el archivo de destino se eliminará automáticamente.

Normalmente, un archivo de captura está preasignado para el segmento de captura más grande previsto y solo una parte de él podría usarse para capturar los datos. Este mensaje solo copia la parte del archivo que contiene los datos de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensajes de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





