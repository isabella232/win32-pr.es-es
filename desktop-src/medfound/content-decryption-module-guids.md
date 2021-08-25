---
description: Los siguientes GUID admiten implementaciones del Módulo de descifrado de contenido (CDM).
title: GUID de módulo de descifrado de contenido (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: ef4016b731b492ed61c6aed859a905446de72c308e03a734aa3cc8f573645668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958785"
---
# <a name="content-decryption-module-cdm-guids"></a>GUID de módulo de descifrado de contenido (CDM)

Los siguientes GUID admiten implementaciones del Módulo de descifrado de contenido (CDM).

**MF_CONTENTDECRYPTIONMODULE_SERVICE**

GUID de servicio que se usa para obtener interfaces de una [implementación de IMFContentDecryptionModule,](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) como la interfaz [IMediaProtectionPMPServer de](/uwp/api/windows.media.protection.mediaprotectionpmpserver) WinRT. Una implementación de **IMFContentDecryptionModule debe** implementar [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) y admitir este GUID de servicio.


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>mfcontentdecryptionmodule.h</dt> </dl> |



## <a name="see-also"></a>Vea también



- [Media Foundation constantes](media-foundation-constants.md)
- [IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-mfcontentdecryptionmodule
- [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




