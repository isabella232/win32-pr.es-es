---
title: Interfaz IDWriteColorGlyphRunEnumerator
description: Esta interfaz permite a la aplicación enumerar a través de las ejecuciones del glifo de color.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Interfaz IDWriteColorGlyphRunEnumerator de escritura directa
- IDWriteColorGlyphRunEnumerator interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802828"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Interfaz IDWriteColorGlyphRunEnumerator

Esta interfaz permite a la aplicación enumerar a través de las ejecuciones del glifo de color. El enumerador enumera las capas de una de vuelta al orden Front para la disposición en capas adecuada.

## <a name="members"></a>Miembros

La interfaz **IDWriteColorGlyphRunEnumerator** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteColorGlyphRunEnumerator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteColorGlyphRunEnumerator** tiene estos métodos.



| Método                                                                | Descripción                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Devuelve la ejecución del glifo actual del enumerador.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Desplácese a la siguiente ejecución del glifo en el enumerador.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

