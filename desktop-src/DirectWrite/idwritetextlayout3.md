---
title: Interfaz IDWriteTextLayout3
description: Representa un bloque de texto una vez que se ha analizado y formateado por completo. | Interfaz IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Interfaz IDWriteTextLayout3 de escritura directa
- IDWriteTextLayout3 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670181"
---
# <a name="idwritetextlayout3-interface"></a>Interfaz IDWriteTextLayout3

Representa un bloque de texto una vez que se ha analizado y formateado por completo.

## <a name="members"></a>Miembros

La interfaz **IDWriteTextLayout3** hereda de [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteTextLayout3** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Recupera las propiedades de cada línea.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Obtiene la información de espaciado de línea.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Invalida el diseño, forzando el diseño para que se remedie antes de llamar a las métricas o funciones de dibujo. Esto resulta útil si el emplazamiento de una fuente cambia y el diseño debe volver a dibujarse, o si el tamaño de un cliente implementa IDWriteInlineObject cambios. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Establezca el interlineado.<br/>                                                                                                                                                                                                                                         |



 

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

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





