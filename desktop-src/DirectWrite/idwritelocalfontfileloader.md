---
title: Interfaz IDWriteLocalFontFileLoader
description: Una implementación integrada de la interfaz IDWriteFontFileLoader, que funciona en archivos de fuentes locales y expone información del archivo de fuente local de la clave de referencia del archivo de fuente.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Escritura directa de la interfaz IDWriteLocalFontFileLoader
- IdWriteLocalFontFileLoader interface Direct Write , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169854"
---
# <a name="idwritelocalfontfileloader-interface"></a>Interfaz IDWriteLocalFontFileLoader

Una implementación integrada de la interfaz [**IDWriteFontFileLoader,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) que funciona en archivos de fuentes locales y expone información del archivo de fuente local de la clave de referencia del archivo de fuente. Las referencias de archivo de fuente [**creadas con CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usan este cargador de archivos de fuente.

## <a name="members"></a>Members

La **interfaz IDWriteLocalFontFileLoader** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteLocalFontFileLoader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteLocalFontFileLoader** tiene estos métodos.



| Método                                                                                  | Descripción                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**GetFilePathFromKey**](idwritelocalfontfileloader-getfilepathfromkey.md)             | Obtiene la ruta de acceso absoluta del archivo de fuente de la clave de referencia del archivo de fuente.<br/>          |
| [**GetFilePathLengthFromKey**](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | Obtiene la longitud de la ruta de acceso absoluta del archivo de la clave de referencia del archivo de fuente.<br/> |
| [**GetLastWriteTimeFromKey**](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | Obtiene la última hora de escritura del archivo a partir de la clave de referencia del archivo de fuente.<br/>      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Dwrite.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



 

