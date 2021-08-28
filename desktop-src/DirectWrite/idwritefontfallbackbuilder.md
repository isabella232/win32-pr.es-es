---
title: Interfaz IDWriteFontFallbackBuilder
description: Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reserva de fuente a partir de esas asignaciones.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Escritura directa de la interfaz IDWriteFontFallbackBuilder
- IdWriteFontFallbackBuilder interface Direct Write , descrito
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
ms.openlocfilehash: 3f42bc9882c238bb1167c76e941c4f183eef05e12d5d8dc70305b0c01e048797
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051404"
---
# <a name="idwritefontfallbackbuilder-interface"></a>Interfaz IDWriteFontFallbackBuilder

Permite crear asignaciones de reserva de fuentes Unicode y crear un objeto de reserva de fuente a partir de esas asignaciones.

## <a name="members"></a>Miembros

La **interfaz IDWriteFontFallbackBuilder** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteFontFallbackBuilder** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IDWriteFontFallbackBuilder** tiene estos métodos.



| Método                                                                      | Descripción                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**AddMapping**](idwritefontfallbackbuilder-addmapping.md)                 | Anexa una asignación única a la lista. Llame a esto una vez para cada asignación adicional.<br/> |
| [**AddMappings**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | Agregue todas las asignaciones de un objeto de reserva de fuente existente.<br/>                       |
| [**CreateFontFallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | Crea el objeto de reserva finalizado a partir de las asignaciones agregadas.<br/>                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

