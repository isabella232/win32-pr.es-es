---
description: Especifica una cadena de contexto usada por las implementaciones del módulo de descifrado de contenido (CDM) que usan MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720472"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a>\_ \_ Propiedad PMPSTORECONTEXT de MF CONTENTDECRYPTIONMODULE

Especifica una cadena de contexto usada por las implementaciones del módulo de descifrado de contenido (CDM) que usan [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).


## <a name="data-type"></a>Tipo de datos

**LPWStr** (VT_LPWSTR)

## <a name="property-guid"></a>GUID de propiedad

**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**

## <a name="property-value"></a>Valor de propiedad

Una cadena de contexto utilizada por las implementaciones del módulo de descifrado de contenido (CDM).

## <a name="remarks"></a>Observaciones

El implementador de CDM debe buscar este valor y pasar el valor al [constructor MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) con el nombre de propiedad "Windows. Media. Protection. PMPStoreContext".


Las aplicaciones no deben crear esta propiedad al llamar a [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Actualización 2020 de abril de Windows 10<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vea también

- [Propiedades de Media Foundation](media-foundation-properties.md)
- [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




