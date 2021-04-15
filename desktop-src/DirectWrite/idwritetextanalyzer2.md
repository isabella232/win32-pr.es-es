---
title: Interfaz IDWriteTextAnalyzer2
description: Analiza varias propiedades de texto para el procesamiento complejo de scripts.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Interfaz IDWriteTextAnalyzer2 de escritura directa
- IDWriteTextAnalyzer2 interface Direct Write, descrito
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534492"
---
# <a name="idwritetextanalyzer2-interface"></a>Interfaz IDWriteTextAnalyzer2

Analiza varias propiedades de texto para el procesamiento complejo de scripts.

## <a name="members"></a>Miembros

La interfaz **IDWriteTextAnalyzer2** hereda de [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1). **IDWriteTextAnalyzer2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteTextAnalyzer2** tiene estos métodos.



| Método                                                                                    | Descripción                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**CheckTypographicFeature**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | Comprueba si una característica tipográfica está disponible para un glifo o un conjunto de glifos.<br/> |
| [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | Devuelve la matriz de transformación de 2x3 para el ángulo respectivo para dibujar la ejecución del glifo.<br/> |
| [**GetTypographicFeatures**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | Devuelve una lista completa de las características OpenType disponibles para un script o una fuente.<br/> |



 

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

[**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

