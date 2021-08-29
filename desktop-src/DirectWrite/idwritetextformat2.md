---
title: Interfaz IDWriteTextFormat2
description: Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional. | Interfaz IDWriteTextFormat2
ms.assetid: 4396d2b0-240f-ee8b-1d21-c4294fb29b51
keywords:
- Direct Write de la interfaz IDWriteTextFormat2
- IdWriteTextFormat2 interface Direct Write , descrito
topic_type:
- apiref
api_name:
- IDWriteTextFormat2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f09e912ca4e019f600ca82886d85392d51a9795fe94a0cdd91b1e94f6a72d2b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649917"
---
# <a name="idwritetextformat2-interface"></a>Interfaz IDWriteTextFormat2

Describe las propiedades de fuente y párrafo utilizadas para dar formato al texto y describe la información de configuración regional.

## <a name="members"></a>Miembros

La **interfaz IDWriteTextFormat2** hereda de [**IDWriteTextFormat1**](idwritetextformat1.md). **IDWriteTextFormat2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteTextFormat2** tiene estos métodos.



| Método                                                      | Descripción                                                                      |
|:------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetLineSpacing**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritetextformat2-getlinespacing) | Obtiene el conjunto de ajuste de espaciado de línea para un párrafo de texto de varias líneas. <br/> |
| [**SetLineSpacing**](idwritetextformat2-setlinespacing.md) | Establecer el espaciado de línea.<br/>                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDWriteTextFormat1**](idwritetextformat1.md)
</dt> </dl>

 

