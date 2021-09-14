---
title: Interfaz IDWriteTextFormat1
description: Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional. | Interfaz IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Escritura directa de la interfaz IDWriteTextFormat1
- IdWriteTextFormat1 interface Direct Write , descrito
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169842"
---
# <a name="idwritetextformat1-interface"></a>Interfaz IDWriteTextFormat1

Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional. Esta interfaz tiene los mismos métodos que [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) y agrega la capacidad de aplicar una orientación explícita.

## <a name="members"></a>Members

La **interfaz IDWriteTextFormat1** hereda de [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat). **IDWriteTextFormat1** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteTextFormat1** tiene estos métodos.



| Método                                                                                | Descripción                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | Obtiene la reserva actual. Si no se estableció ninguna desde la creación del diseño, será nullptr.<br/>               |
| [**GetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | Obtiene el modo de ajuste de la última línea.<br/>                                                                     |
| [**GetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | Obtiene la alineación del margen óptico para el formato de texto.<br/>                                                       |
| [**GetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | Obtiene la orientación preferida de los glifos cuando se usa una dirección de lectura vertical.<br/>                             |
| [**SetFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | Aplica la reserva de fuente personalizada al diseño. Si no se establece ninguno, usa la lista de reserva del sistema predeterminada. <br/> |
| [**SetLastLineWrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | Establece el modo de ajuste de la última línea.<br/>                                                                     |
| [**SetOpticalAlignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | Establece la alineación del margen óptico para el formato de texto.<br/>                                                       |
| [**SetVerticalGlyphOrientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | Establece la orientación de un formato de texto.<br/>                                                                       |



 

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

[**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

