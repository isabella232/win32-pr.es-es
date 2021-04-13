---
title: Interfaz IDWriteTextLayout2
description: Representa un bloque de texto una vez que se ha analizado y formateado por completo. | Interfaz IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Interfaz IDWriteTextLayout2 de escritura directa
- IDWriteTextLayout2 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362255"
---
# <a name="idwritetextlayout2-interface"></a>Interfaz IDWriteTextLayout2

Representa un bloque de texto una vez que se ha analizado y formateado por completo.

## <a name="members"></a>Miembros

La interfaz **IDWriteTextLayout2** hereda de [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1). **IDWriteTextLayout2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteTextLayout2** tiene estos métodos.



| Método                                                                                | Descripción                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Obtiene el objeto de reserva de fuente actual. <br/>                                           |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Obtiene si se ajusta o no la última palabra de la última línea.<br/>                    |
| [**GetMetrics**](idwritetextlayout2-getmetrics.md)                                   | Recupera las métricas generales de la cadena con formato. <br/>                             |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Obtiene el modo en que los glifos se alinean con los bordes del margen. <br/>                               |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Obtiene la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.<br/> |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Aplicar una reserva de fuentes personalizada en el diseño.<br/>                                        |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Establece si se ajusta o no la última palabra de la última línea. <br/>                   |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Establece cómo se alinean los glifos con los bordes del margen.<br/>                                |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Establecer la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

