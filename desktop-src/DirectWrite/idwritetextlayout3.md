---
title: Interfaz IDWriteTextLayout3
description: Representa un bloque de texto después de que se haya analizado y dado formato por completo. | Interfaz IDWriteTextLayout3
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- Escritura directa de la interfaz IDWriteTextLayout3
- IdWriteTextLayout3 interface Direct Write , descrito
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
ms.openlocfilehash: 9f3a6d441c3f7d8ac9bf356bd835f800e026f8c6e27cb083a57ced571ba68fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070655"
---
# <a name="idwritetextlayout3-interface"></a>Interfaz IDWriteTextLayout3

Representa un bloque de texto después de que se haya analizado y dado formato por completo.

## <a name="members"></a>Miembros

La **interfaz IDWriteTextLayout3** hereda de [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteTextLayout3** tiene estos métodos.



| Método                                                          | Descripción                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Recupera las propiedades de cada línea.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Obtiene información de espaciado de línea.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Invalida el diseño, lo que obliga a que el diseño se reemita antes de llamar a las métricas o a las funciones de dibujo. Esto resulta útil si cambia la localidad de una fuente y se debe volver a dibujar el diseño, o si cambia el tamaño de un cliente implementado por IDWriteInlineObject. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Establezca el espaciado de línea.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





