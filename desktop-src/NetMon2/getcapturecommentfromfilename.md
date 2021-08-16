---
description: La función GetCaptureCommentFromFilename extrae el comentario de captura de un archivo de captura.
ms.assetid: d3665cb0-d54d-45f7-aef9-c2e603d6f773
title: Función GetCaptureCommentFromFilename (Netmon.h)
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
ms.openlocfilehash: 1b92b81fa00834c3a4038a6a6bb9f295246a7c0b217c99779a5d2c569dbbf982
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118366816"
---
# <a name="getcapturecommentfromfilename-function"></a>Función GetCaptureCommentFromFilename

La **función GetCaptureCommentFromFilename** extrae el comentario de captura de un [*archivo de captura.*](c.md)

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

*lpFilename* \[ En\]
</dt> <dd>

Puntero al nombre del archivo de captura.

</dd> <dt>

*lpComment* \[ En\]
</dt> <dd>

Puntero a una cadena preasignada para el comentario.

</dd> <dt>

*BufferSize* \[ En\]
</dt> <dd>

Tamaño de la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (es decir, si el comentario se encuentra y se copia, o no hay ningún comentario en el archivo de captura), el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error.



| Código devuelto                                                                                                 | Descripción                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**ERROR DE LECTURA \_ DEL ARCHIVO NMERR \_ \_**</dt> </dl>     | No se puede leer el comentario de captura.<br/>                               |
| <dl> <dt>**FORMATO DE ARCHIVO \_ NO \_ VÁLIDO DE \_ NMERR**</dt> </dl> | El marco Comentario no es un formato de archivo válido.<br/>                     |
| <dl> <dt>**ARCHIVO NMERR \_ \_ NO \_ ENCONTRADO**</dt> </dl>      | No se encuentra el archivo especificado *por el parámetro lpFilename.*<br/> |
| <dl> <dt>**NMERR \_ INVALID \_ PARAMETER**</dt> </dl>    | Uno de los parámetros se especifica incorrectamente.<br/>                   |



 

## <a name="remarks"></a>Comentarios

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a la **función GetCaptureCommentFromFilename.**

Para recuperar el comentario de una captura en tiempo real, llame a la [función GetCaptureComment.](getcapturecomment.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[GetCaptureComment](getcapturecomment.md)
</dt> </dl>

 

 




