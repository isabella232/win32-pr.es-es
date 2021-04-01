---
title: Interfaz IDWriteFontFallbackBuilder
description: Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reversión de fuente a partir de esas asignaciones.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Interfaz IDWriteFontFallbackBuilder de escritura directa
- IDWriteFontFallbackBuilder interface Direct Write, descrito
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996628"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Interfaz IDWriteFontFallbackBuilder

Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reversión de fuente a partir de esas asignaciones.

## <a name="members"></a>Miembros

La interfaz **IDWriteFontFallbackBuilder** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IDWriteFontFallbackBuilder** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDWriteFontFallbackBuilder** tiene estos métodos.



| Método                                                                      | Descripción                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Anexa una única asignación a la lista. Llame a este método una vez por cada asignación adicional.<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Agregue todas las asignaciones de un objeto de reserva de fuente existente.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Crea el objeto de reserva finalizado a partir de las asignaciones agregadas.<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

