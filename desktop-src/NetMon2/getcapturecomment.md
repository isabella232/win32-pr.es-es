---
description: Devuelve un puntero al comentario de una captura.
ms.assetid: 3ef5c5b3-5586-469f-8975-049713715403
title: Función GetCaptureComment (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171466"
---
# <a name="getcapturecomment-function"></a>Función GetCaptureComment

La **función GetCaptureComment** devuelve un puntero al comentario de una captura.

## <a name="syntax"></a>Sintaxis


```C++
LPSTR WINAPI GetCaptureComment(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCapture* \[ En\]
</dt> <dd>

Identificador de la captura. Para obtener más información sobre cómo obtener el identificador de captura, vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente (es decir, si la captura contiene un comentario), el valor devuelto es un puntero a la cadena de comentario.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

No modifique la cadena de comentario devuelta, que es la cadena de comentario real que se encuentra en la captura cargada. Los cambios pueden dañar la captura. Los intentos de modificar la cadena tienen como resultado una infracción de acceso.

El identificador de la captura se puede obtener de varias maneras, dependiendo de si la llamada la realiza un experto o un analizador. Para los expertos, el identificador se especifica en el **miembro hCapture** de la [estructura EXPERTSTARTUPINFO.](expertstartupinfo.md) Para los analizadores, el identificador de captura se puede obtener llamando a la [función GetFrameCaptureHandle.](getframecapturehandle.md)

Para recuperar el comentario de una captura de su archivo de captura, llame a la [función GetCaptureCommentFromFilename.](getcapturecommentfromfilename.md)

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetCaptureComment.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[EXPERTSTARTUPINFO](expertstartupinfo.md)
</dt> <dt>

[GetCaptureCommentFromFilename](getcapturecommentfromfilename.md)
</dt> <dt>

[GetFrameCaptureHandle](getframecapturehandle.md)
</dt> </dl>

 

 




