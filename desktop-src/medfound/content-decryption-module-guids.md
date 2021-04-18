---
description: Los siguientes GUID admiten implementaciones del módulo de descifrado de contenido (CDM).
title: GUID de módulo de descifrado de contenido (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721593"
---
# <a name="content-decryption-module-cdm-guids"></a>GUID de módulo de descifrado de contenido (CDM)

Los siguientes GUID admiten implementaciones del módulo de descifrado de contenido (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

GUID de servicio usado para obtener interfaces de una implementación de [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , como la interfaz [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) de WinRT. Una implementación de **IMFContentDecryptionModule** debe implementar [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) y admitir este GUID de servicio.


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>mfcontentdecryptionmodule. h</dt> </dl> |



## <a name="see-also"></a>Vea también



- [Constantes de Media Foundation](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




