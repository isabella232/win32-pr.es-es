---
title: Interfaz IDWriteColorGlyphRunEnumerator
description: Esta interfaz permite a la aplicación enumerar a través de las ejecuciones de glifo de color.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- IDWriteColorGlyphRunEnumerator interface Direct Write
- IdWriteColorGlyphRunEnumerator interface Direct Write , descrito
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
ms.openlocfilehash: 8fa665f7000ffaada5bc14f97671fb6e52266c712ef6081b956184653d1f1c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536145"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Interfaz IDWriteColorGlyphRunEnumerator

Esta interfaz permite a la aplicación enumerar a través de las ejecuciones de glifo de color. El enumerador enumera las capas en orden de vuelta al orden de entrada para la capa adecuada.

## <a name="members"></a>Miembros

La **interfaz IDWriteColorGlyphRunEnumerator** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteColorGlyphRunEnumerator** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteColorGlyphRunEnumerator** tiene estos métodos.



| Método                                                                | Descripción                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Devuelve la ejecución del glifo actual del enumerador.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Pase a la siguiente ejecución de glifo en el enumerador.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

