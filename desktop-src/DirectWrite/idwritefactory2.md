---
title: Interfaz IDWriteFactory2
description: La interfaz de fábrica raíz para todos los objetos de DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Interfaz IDWriteFactory1 de escritura directa
- IDWriteFactory1 interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686048"
---
# <a name="idwritefactory2-interface"></a>Interfaz IDWriteFactory2

La interfaz de fábrica raíz para todos los objetos de [DirectWrite](direct-write-portal.md) .

## <a name="members"></a>Miembros

La interfaz **IDWriteFactory1** hereda de [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1). **IDWriteFactory2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteFactory1** tiene estos métodos.



| Método                                                                             | Descripción                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CreateCustomRenderingParams**](idwritefactory2-createcustomrenderingparams.md) | Crea un objeto de parámetros de representación con las propiedades especificadas.<br/>                            |
| [**CreateFontFallbackBuilder**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | Crea un objeto de generador de reserva de fuentes.<br/>                                                         |
| [**CreateGlyphRunAnalysis**](idwritefactory2-createglyphrunanalysis.md)           | Crea un objeto de análisis de ejecución de glifos, que encapsula la información utilizada para representar una ejecución de glifo.<br/> |
| [**GetSystemFontFallback**](idwritefactory2-getsystemfontfallback.md)             | Crea un objeto de reserva de fuente a partir de la lista de reserva del sistema.<br/>                              |
| [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | Se llama a este método en una ejecución de glifo para convertirlo en ejecuciones de glifo de varios colores.<br/>           |



 

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

[**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

