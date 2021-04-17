---
description: Devuelve un puntero al comentario de una captura.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Función GetCaptureComment (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureComment
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ca2d3dd3fdc91c54c49b12119a56180396df5ec5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666285"
---
# <a name="getcapturecomment-function"></a>GetCaptureComment función)

La función **GetCaptureComment** devuelve un puntero al comentario de una captura.

## <a name="syntax"></a>Sintaxis


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ de\]
</dt> <dd>

Identificador de la captura. Para obtener más información sobre cómo obtener el identificador de captura, vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta (es decir, si la captura contiene un comentario), el valor devuelto es un puntero a la cadena de comentario.

Si la función no se realiza correctamente, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

No modifique la cadena de comentario devuelta, que es la cadena de comentario real que se encuentra en la captura cargada. Cualquier cambio puede dañar la captura. Los intentos de modificar la cadena producen una infracción de acceso.

El identificador de la captura se puede obtener de varias maneras, dependiendo de si el experto o el analizador realizan la llamada. En el caso de los expertos, el identificador se especifica en el miembro **hCapture** de la estructura [EXPERTSTARTUPINFO](expertstartupinfo.md) . En el caso de los analizadores, el identificador de captura se puede obtener llamando a la función [GetFrameCaptureHandle](getframecapturehandle.md) .

Para recuperar el comentario de una captura de su archivo de captura, llame a la función [GetCaptureCommentFromFilename](getcapturecommentfromfilename.md) .

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureComment** .

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

[EXPERTSTARTUPINFO](expertstartupinfo.md)
</dt> <dt>

[GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)
</dt> <dt>

[GetFrameCaptureHandle](getframecapturehandle.md)
</dt> </dl>

 

 




