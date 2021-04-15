---
description: La función GetCaptureCommentFromFilename extrae el comentario de captura de un archivo de captura.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Función GetCaptureCommentFromFilename (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureCommentFromFilename
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 9dbfb086ccc27ad2f4c35018c3384a4b81ef0528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677283"
---
# <a name="getcapturecommentfromfilename-function"></a>GetCaptureCommentFromFilename función)

La función **GetCaptureCommentFromFilename** extrae el comentario de captura de un [*archivo de captura*](c.md).

## <a name="syntax"></a>Sintaxis


```C++
DWORD  WINAPI GetCaptureCommentFromFilename(
  _In_ LPSTR lpFilename,
  _In_ LPSTR lpComment,
  _In_ DWORD BufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpFilename* \[ de\]
</dt> <dd>

Puntero al nombre del archivo de captura.

</dd> <dt>

*lpComment* \[ de\]
</dt> <dd>

Puntero a una cadena asignada previamente para el comentario.

</dd> <dt>

*BufferSize* \[ de\]
</dt> <dd>

Tamaño de la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si se encuentra el comentario y se copia, o si no hay ningún comentario en el archivo de captura), el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un código de error.



| Código devuelto                                                                                                 | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**\_error de \_ lectura del archivo NMERR \_**</dt> </dl>     | No se puede leer el comentario de captura.<br/>                               |
| <dl> <dt>**NMERR \_ \_ formato de archivo no válido \_**</dt> </dl> | El marco del comentario no es un formato de archivo válido.<br/>                     |
| <dl> <dt>**\_ \_ no \_ se encontró el archivo NMERR**</dt> </dl>      | No se encuentra el archivo especificado por el parámetro *lpFilename* .<br/> |
| <dl> <dt>**NMERR \_ parámetro no válido \_**</dt> </dl>    | Uno de los parámetros no se ha especificado correctamente.<br/>                   |



 

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureCommentFromFilename** .

Para recuperar el comentario de una captura en tiempo real, llame a la función [GetCaptureComment](getcapturecomment.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




