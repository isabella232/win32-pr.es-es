---
title: Propiedades de DRM
description: Propiedades de DRM
ms.assetid: 862fc8bc-6e40-4496-862a-c12c8a382116
keywords:
- Windows SDK de formato multimedia, propiedades drm
- Formato de sistemas avanzados (ASF), propiedades drm
- ASF (formato de sistemas avanzados), propiedades drm
- administración de derechos digitales (DRM), propiedades
- DRM (administración de derechos digitales), propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8542d360c38ab3f12406462cefc0454e7eae33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359921"
---
# <a name="drm-properties"></a>Propiedades de DRM

En la tabla siguiente se enumeran las propiedades drm que las aplicaciones pueden obtener o establecer al escribir o leer archivos protegidos. Estas propiedades no son atributos de archivo; no se escriben en el encabezado de archivo ASF.



| Propiedad DRM                                                                             | Identificador global                               | Tipo de datos             |
|------------------------------------------------------------------------------------------|-------------------------------------------------|-----------------------|
| [**Acción \_ de DRMAllowed**](drm-actionallowed.md)                                          | g \_ wszWMDRM \_ ActionAllowed                      | **WMT \_ TYPE \_ BOOL**   |
| [**Acción de \_ DRMAllowed \_ Backup**](drm-actionallowed-backup.md)                           | g \_ wszWMDRM \_ ActionAllowed \_ Backup              | **WMT \_ TYPE \_ BOOL**   |
| [**Acción \_ drmAllowed \_ CollaborativePlay**](drm-actionallowed-collaborativeplay.md)     | g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay   | **WMT \_ TYPE \_ BOOL**   |
| [**Acción \_ de DRMAllowed \_ Copy**](drm-actionallowed-copy.md)                               | g \_ wszWMDRM \_ ActionAllowed \_ Copy                | **WMT \_ TYPE \_ BOOL**   |
| [**Acción \_ drmAllowed \_ CopyToCD**](drm-actionallowed-copytocd.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToCD            | **WMT \_ TYPE \_ BOOL**   |
| [**Acción \_ de DRMAllowed \_ CopyToNonSDMIDevice**](drm-actionallowed-copytononsdmidevice.md) | g \_ wszWMDRM \_ ActionAllowed \_ CopyToNonSDMIDevice | **WMT \_ TYPE \_ BOOL**   |
| [**Acción \_ drmAllowed \_ CopyToSDMIDevice**](drm-actionallowed-copytosdmidevice.md)       | g \_ wszWMDRM \_ ActionAllowed \_ CopyToSDMIDevice    | **WMT \_ TYPE \_ BOOL**   |
| [**Acción de \_ DRMAprobación \_ permitido**](drm-actionallowed-playback.md)                       | g \_ wszWMDRM \_ ActionAllowed \_ Playback            | **WMT \_ TYPE \_ BOOL**   |
| [**Acción de \_ DRMAllowed \_ Playlist (Lista de reproducción permitido)**](drm-actionallowed-playlistburn.md)               | g \_ wszWMDRM ActionAllowed Playlist (Acción wszWMDRM)Lista \_ de reproducción \_ permitido        | **WMT \_ TYPE \_ BOOL**   |
| [**DRM \_ BaseLicenseAcqURL**](drm-baselicenseacqurl.md)                                  | g \_ wszWMDRM \_ BaseLicenseAcqURL                  | **CADENA DE TIPO WMT \_ \_** |
| [**Marcas \_ DRM**](drm-flags.md)                                                          | g \_ wszWMDRM \_ Flags                              | **DWORD \_ DE TIPO \_ WMT**  |
| [**Encabezado \_ DRMSignPrivKey**](drm-headersignprivkey.md)                                  | g \_ wszWMDRM \_ HeaderSignPrivKey                  | **CADENA DE TIPO WMT \_ \_** |
| [**DRM \_ IsDRM**](drm-isdrm.md)                                                          | g \_ wszIsDRM                                     | **WMT \_ TYPE \_ BOOL**   |
| [**DRM \_ IsDRMCached**](drm-isdrmcached.md)                                              | g \_ wszIsDRMCached                               | **WMT \_ TYPE \_ BOOL**   |
| [**DRM \_ KeySeed**](drm-keyseed.md)                                                      | g \_ wszWMDRM \_ KeySeed                            | **CADENA DE TIPO WMT \_ \_** |
| [**Nivel de \_ DRM**](drm-level.md)                                                          | g \_ wszWMDRM \_ Level                              | **DWORD \_ DE TIPO \_ WMT**  |
| [**LicenseID de DRM \_**](drm-licenseid.md)                                                  | g \_ wszWMDRM \_ LicenseID                          | **CADENA DE TIPO WMT \_ \_** |
| [**DRM \_ LicenseState**](drm-licensestate.md)                                            | g \_ wszWMDRM \_ LicenseState                       | **DWORD \_ DE TIPO \_ WMT**  |
| [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)       | g \_ wszWMDRM \_ LicenseState \_ CollaborativePlay    | **BINARIO DE \_ TIPO \_ WMT** |
| [**\_Copia de LicenseState de DRM \_**](drm-licensestate-copy.md)                                 | g \_ wszWMDRM \_ LicenseState \_ Copy                 | **BINARIO DE \_ TIPO \_ WMT** |
| [**\_LicenseState \_ CopyToCD de DRM**](drm-licensestate-copytocd.md)                         | g \_ wszWMDRM \_ LicenseState \_ CopyToCD             | **BINARIO DE \_ TIPO \_ WMT** |
| [**\_LicenseState \_ CopyToSDMIDevice de DRM**](drm-licensestate-copytosdmidevice.md)         | g \_ wszWMDRM \_ LicenseState \_ CopyToSDMIDevice     | **BINARIO DE \_ TIPO \_ WMT** |
| [**\_LicenseState \_ copyToNonSDMIDevice de DRM**](drm-licensestate-copytononsdmidevice.md)   | g \_ wszWMDRM \_ LicenseState \_ CopyToNonSDMIDevice  | **BINARIO DE \_ TIPO \_ WMT** |
| [**\_Reproducción de Drm LicenseState \_**](drm-licensestate-playback.md)                         | g \_ wszWMDRM \_ LicenseState \_ Playback             | **BINARIO DE \_ TIPO \_ WMT** |
| [**Lista \_ de reproducción de DRM LicenseState \_**](drm-licensestate-playlistburn.md)                 | g \_ wszWMDRM LicenseState Playlist (Lista de reproducción de g wszWMDRM \_ \_ LicenseState)         | **BINARIO DE \_ TIPO \_ WMT** |
| [**Derechos de DRM \_**](drm-rights.md)                                                        | g \_ wszWMDRM \_ Rights                             | **CADENA DE TIPO WMT \_ \_** |
| [**DRM \_ SAPLEVEL**](drm-saplevel--deprecated.md)                                        | g \_ wszWMDRM \_ SAPLEVEL                           | **CADENA DE TIPO WMT \_ \_** |
| [**Uso \_ de \_ DRM avanzado**](use-advanced-drm.md)                                           | g \_ wszWMUse \_ Advanced \_ DRM                      | **WMT \_ TYPE \_ BOOL**   |
| [**Uso de \_ DRM**](use-drm.md)                                                              | g \_ wszWMUse \_ DRM                                | **WMT \_ TYPE \_ BOOL**   |
| [**Revocación de \_ WMDRMNET**](wmdrmnet-revocation.md)                                      | g \_ wszWMDRMNET \_ Revocation                      | **CADENA DE TIPO WMT \_ \_** |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lista de atributos DRM**](drm-attribute-list.md)
</dt> </dl>

 

 




