---
title: Propiedades de DRM
description: Propiedades de DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows SDK de formato multimedia, propiedades de DRM
- Formato de sistemas avanzados (ASF), propiedades drm
- ASF (formato de sistemas avanzados), propiedades drm
- administración de derechos digitales (DRM),properties
- DRM (administración de derechos digitales),propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d553d644a6f3ec7130262d0e8567a4aa6ceab53286b24248607b1928991f51d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848271"
---
# <a name="drm-properties"></a>Propiedades de DRM

En la tabla siguiente se enumeran las propiedades de DRM que las aplicaciones pueden obtener o establecer al escribir o leer archivos protegidos. Estas propiedades no son atributos de archivo; no se escriben en el encabezado de archivo ASF.



| Propiedad DRM                                                                             | Identificador global                               | Tipo de datos             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**Acción \_ drmAllowed**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **TIPO WMT \_ \_ BOOL**   |
| [**Acción \_ DRMAllowed \_ Backup**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ Backup              | **TIPO WMT \_ \_ BOOL**   |
| [**Acción \_ drmAllowed \_ CollaborativePlay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **TIPO WMT \_ \_ BOOL**   |
| [**Acción \_ de DRMAllowed \_ Copy**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_ Copy                | **TIPO WMT \_ \_ BOOL**   |
| [**Acción \_ de DRMAllowed \_ CopyToCD**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **TIPO WMT \_ \_ BOOL**   |
| [**Acción \_ de DRMAllowed \_ CopyToNonSDMIDevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **TIPO WMT \_ \_ BOOL**   |
| [**Acción \_ de DRMAllowed \_ CopyToSDMIDevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **TIPO WMT \_ \_ BOOL**   |
| [**Acción de \_ DRMAllowed \_ Playback**](drm-actionallowed-playback.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ Playback            | **TIPO WMT \_ \_ BOOL**   |
| [**Acción de \_ DRMAllowed Playlist Playlist (Lista de \_ reproducción permitido)**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM \_ ActionAllowed Playlist (Lista de reproducción \_ permitido)        | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ BaseLicenseAcqURL**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **CADENA DE \_ TIPO \_ WMT** |
| [**Marcas \_ DRM**](drm-flags.md)                                                          | g \_ wszWMDRM \_ Flags                              | **DWORD \_ DE TIPO \_ WMT**  |
| [**Encabezado \_ DRMSignPrivKey**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **CADENA DE \_ TIPO \_ WMT** |
| [**DRM \_ IsDRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ IsDRMCached**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **TIPO WMT \_ \_ BOOL**   |
| [**DRM \_ KeySeed**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ KeySeed                            | **CADENA DE \_ TIPO \_ WMT** |
| [**Nivel de \_ DRM**](drm-level.md)                                                          | g \_ wszWMDRM \_ Level                              | **DWORD \_ DE TIPO \_ WMT**  |
| [**Id. de licencia de DRM \_**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **CADENA DE \_ TIPO \_ WMT** |
| [**DRM \_ LicenseState**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **DWORD \_ DE TIPO \_ WMT**  |
| [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **BINARIO DE \_ TIPO \_ WMT** |
| [**Copia \_ de LicenseState de DRM \_**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_ Copy                 | **BINARIO DE \_ TIPO \_ WMT** |
| [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **BINARIO DE \_ TIPO \_ WMT** |
| [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **BINARIO DE \_ TIPO \_ WMT** |
| [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **BINARIO DE \_ TIPO \_ WMT** |
| [**DRM \_ LicenseState \_ Playback**](drm-licensestate-playback.md)                         | g \_ wszWMDRM \_ LicenseState \_ Playback             | **BINARIO DE \_ TIPO \_ WMT** |
| [**Lista \_ de reproducción de DRM LicenseState \_**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM LicenseState Playlist Playlist Playlist (Lista de reproducción de wszWMDRM \_ \_ LicenseState)         | **BINARIO DE \_ TIPO \_ WMT** |
| [**Derechos de \_ DRM**](drm-rights.md)                                                        | g \_ wszWMDRM \_ Rights                             | **CADENA DE \_ TIPO \_ WMT** |
| [**DRM \_ SAPLEVEL**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **CADENA DE \_ TIPO \_ WMT** |
| [**Uso \_ de \_ DRM avanzado**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ Advanced \_ DRM                      | **TIPO WMT \_ \_ BOOL**   |
| [**Uso de \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **TIPO WMT \_ \_ BOOL**   |
| [**Revocación de \_ WMDRMNET**](wmdrmnet-revocation.md)                                      | g \_ wszWMDRMNET \_ Revocation                      | **CADENA DE \_ TIPO \_ WMT** |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> </dl>

 

 




