---
title: Interfaz IDWriteTextAnalyzer2
description: Analiza varias propiedades de texto para el procesamiento de scripts complejos.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Escritura directa de la interfaz IDWriteTextAnalyzer2
- IdWriteTextAnalyzer2 interface Direct Write , descrito
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169845"
---
# <a name="idwritetextanalyzer2-interface"></a>Interfaz IDWriteTextAnalyzer2

Analiza varias propiedades de texto para el procesamiento de scripts complejos.

## <a name="members"></a>Members

La **interfaz IDWriteTextAnalyzer2** hereda de [**IDWriteTextAnalyzer1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) **IDWriteTextAnalyzer2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteTextAnalyzer2** tiene estos métodos.



| Método                                                                                    | Descripción                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**CheckTypographicFeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Comprueba si una característica tipográfica está disponible para un glifo o un conjunto de glifos.<br/> |
| [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Devuelve una matriz de transformación de 2x3 para el ángulo respectivo para dibujar la ejecución del glifo.<br/> |
| [**GetTypographicFeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Devuelve una lista completa de las características de OpenType disponibles para un script o fuente.<br/> |



 

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

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

