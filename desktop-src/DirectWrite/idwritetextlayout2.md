---
title: Interfaz IDWriteTextLayout2
description: Representa un bloque de texto después de que se haya analizado y dado formato por completo. | Interfaz IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Escritura directa de la interfaz IDWriteTextLayout2
- IdWriteTextLayout2 interface Direct Write , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169826"
---
# <a name="idwritetextlayout2-interface"></a>Interfaz IDWriteTextLayout2

Representa un bloque de texto después de que se haya analizado y dado formato por completo.

## <a name="members"></a>Members

La **interfaz IDWriteTextLayout2** hereda de [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1). **IDWriteTextLayout2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteTextLayout2** tiene estos métodos.



| Método                                                                                | Descripción                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Obtiene el objeto de reserva de fuente actual. <br/>                                           |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Obtenga si la última palabra de la última línea está ajustada o no.<br/>                    |
| [**GetMetrics**](idwritetextlayout2-getmetrics.md)                                   | Recupera las métricas generales de la cadena con formato. <br/>                             |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Obtenga cómo se alinean los glifos con los bordes del margen. <br/>                               |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Obtiene la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.<br/> |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Aplicar una reserva de fuente personalizada al diseño.<br/>                                        |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Establezca si se ajusta o no la última palabra de la última línea. <br/>                   |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Establezca cómo se alinean los glifos con los bordes del margen.<br/>                                |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Establezca la orientación preferida de los glifos al usar una dirección de lectura vertical.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

