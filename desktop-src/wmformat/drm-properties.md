---
title: Propiedades de DRM
description: Propiedades de DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- SDK de Windows Media Format, propiedades de DRM
- Advanced Systems Format (ASF), propiedades de DRM
- ASF (formato de sistemas avanzados), propiedades de DRM
- Administración de derechos digitales (DRM), propiedades
- DRM (administración de derechos digitales), propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8542d360c38ab3f12406462cefc0454e7eae33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076384"
---
# <a name="drm-properties"></a>Propiedades de DRM

En la tabla siguiente se enumeran las propiedades DRM que las aplicaciones pueden obtener o establecer al escribir o leer archivos protegidos. Estas propiedades no son atributos de archivo; no se escriben en el encabezado de archivo ASF.



| Propiedad DRM                                                                             | Identificador global                               | Tipo de datos             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**\_ACTIONALLOWED DRM**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **tipo de WMT \_ \_ bool**   |
| [**Copia de seguridad de \_ ActionAllowed de DRM \_**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ backup              | **tipo de WMT \_ \_ bool**   |
| [**\_CollaborativePlay ACTIONALLOWED \_ DRM**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **tipo de WMT \_ \_ bool**   |
| [**\_Copia de ActionAllowed de DRM \_**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_                | **tipo de WMT \_ \_ bool**   |
| [**\_CopyToCD ACTIONALLOWED \_ DRM**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **tipo de WMT \_ \_ bool**   |
| [**\_CopyToNonSDMIDevice ACTIONALLOWED \_ DRM**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **tipo de WMT \_ \_ bool**   |
| [**\_CopyToSDMIDevice ACTIONALLOWED \_ DRM**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **tipo de WMT \_ \_ bool**   |
| [**\_Reproducción de ACTIONALLOWED DRM \_**](drm-actionallowed-playback.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ reproducción            | **tipo de WMT \_ \_ bool**   |
| [**\_PlaylistBurn ACTIONALLOWED \_ DRM**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed \_ PlaylistBurn        | **tipo de WMT \_ \_ bool**   |
| [**\_BASELICENSEACQURL DRM**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **\_cadena de tipo WMT \_** |
| [**\_Marcas DRM**](drm-flags.md)                                                          | g \_ marcas de wszWMDRM \_                              | **tipo de WMT \_ \_ DWORD**  |
| [**\_HEADERSIGNPRIVKEY DRM**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **\_cadena de tipo WMT \_** |
| [**\_ISDRM DRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **tipo de WMT \_ \_ bool**   |
| [**\_ISDRMCACHED DRM**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **tipo de WMT \_ \_ bool**   |
| [**\_KEYSEED DRM**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ KeySeed                            | **\_cadena de tipo WMT \_** |
| [**Nivel de DRM \_**](drm-level.md)                                                          | \_nivel g wszWMDRM \_                              | **tipo de WMT \_ \_ DWORD**  |
| [**\_LICENSEID DRM**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **\_cadena de tipo WMT \_** |
| [**\_LICENSESTATE DRM**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **tipo de WMT \_ \_ DWORD**  |
| [**\_CollaborativePlay LICENSESTATE \_ DRM**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **tipo de WMT \_ \_ binario** |
| [**\_Copia de LicenseState de DRM \_**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_                 | **tipo de WMT \_ \_ binario** |
| [**\_CopyToCD LICENSESTATE \_ DRM**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **tipo de WMT \_ \_ binario** |
| [**\_CopyToSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **tipo de WMT \_ \_ binario** |
| [**\_CopyToNonSDMIDevice LICENSESTATE \_ DRM**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **tipo de WMT \_ \_ binario** |
| [**\_Reproducción de LICENSESTATE DRM \_**](drm-licensestate-playback.md)                         | g \_ wszWMDRM \_ LicenseState \_ reproducción             | **tipo de WMT \_ \_ binario** |
| [**\_PlaylistBurn LICENSESTATE \_ DRM**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM \_ LicenseState \_ PlaylistBurn         | **tipo de WMT \_ \_ binario** |
| [**Derechos de DRM \_**](drm-rights.md)                                                        | g \_ wszWMDRM \_ derechos                             | **\_cadena de tipo WMT \_** |
| [**\_SAPLEVEL DRM**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **\_cadena de tipo WMT \_** |
| [**Usar \_ \_ DRM avanzada**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ \_ DRM avanzada                      | **tipo de WMT \_ \_ bool**   |
| [**Usar \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **tipo de WMT \_ \_ bool**   |
| [**Revocación de WMDRMNET \_**](wmdrmnet-revocation.md)                                      | g \_ \_ revocación de wszWMDRMNET                      | **\_cadena de tipo WMT \_** |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos de DRM**](drm-attribute-list.md)
</dt> </dl>

 

 




