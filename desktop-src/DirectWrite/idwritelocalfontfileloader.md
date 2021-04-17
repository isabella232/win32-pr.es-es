---
title: Interfaz IDWriteLocalFontFileLoader
description: Implementación integrada de la interfaz IDWriteFontFileLoader, que funciona en archivos de fuentes locales y expone información del archivo de fuentes local a partir de la clave de referencia del archivo de fuente.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Interfaz IDWriteLocalFontFileLoader de escritura directa
- IDWriteLocalFontFileLoader interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671035"
---
# <a name="idwritelocalfontfileloader-interface"></a>Interfaz IDWriteLocalFontFileLoader

Implementación integrada de la interfaz [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , que funciona en archivos de fuentes locales y expone información del archivo de fuentes local a partir de la clave de referencia del archivo de fuente. Las referencias de archivo de fuentes creadas con [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usan este cargador de archivos de fuentes.

## <a name="members"></a>Miembros

La interfaz **IDWriteLocalFontFileLoader** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteLocalFontFileLoader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteLocalFontFileLoader** tiene estos métodos.



| Método                                                                                  | Descripción                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Obtiene la ruta de acceso del archivo de fuentes absolutas de la clave de referencia del archivo de fuente.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Obtiene la longitud de la ruta de acceso absoluta del archivo a partir de la clave de referencia del archivo de fuente.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Obtiene la hora de la última escritura del archivo a partir de la clave de referencia del archivo de fuente.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

