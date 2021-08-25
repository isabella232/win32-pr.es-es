---
title: Interfaces de cliente drm Windows multimedia de Microsoft
description: Interfaces de cliente drm Windows multimedia de Microsoft
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows SDK de formato multimedia, interfaces
- administración de derechos digitales (DRM), interfaces
- DRM (administración de derechos digitales), interfaces
- API extendidas de cliente DRM, interfaces
- API extendidas de cliente, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972224decdad339876e4f72c40cad5b3ba28de98446ff358fd36cb7f86bee0af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931105"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Interfaces de cliente drm Windows multimedia de Microsoft

En la tabla siguiente se describen las interfaces admitidas por Windows API de cliente DRM de multimedia.



| Interfaz                                                                    | Descripción                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Proporciona la definición de una devolución de llamada de estado que puede implementar para controlar las operaciones DRM asincrónicas.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Proporciona un método para descifrar el contenido.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Proporciona un método para cifrar los datos en su lugar.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Cifra los datos de bloques no contiguos.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Extensión de la **interfaz IMFMediaEventGenerator que** proporciona un método para cancelar operaciones asincrónicas. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Habilita la recuperación de información de estado avanzada sobre el progreso de la individualización.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Representa una o varias licencias en el almacén de licencias local.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Habilita la recuperación de información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Habilita las operaciones de administración para el almacén de licencias local.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Proporciona opciones de administración adicionales para el almacén de licencias local.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Permite a las aplicaciones consultar los derechos y el estado de licencia de un archivo protegido.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | Proporciona los métodos necesarios para crear una aplicación receptora Windows DRM multimedia de Microsoft para dispositivos de red.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | Proporciona los métodos necesarios para crear una aplicación de transmisor drm Windows multimedia de Microsoft para dispositivos de red.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Proporciona métodos que permiten la adquisición de licencias con la intervención del usuario.                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | Crea los demás objetos de las API extendidas de Windows DRM multimedia de Microsoft.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Administra varios procesos relacionados con la seguridad para el equipo cliente y el subsistema DRM.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Administra la revocación y renovación de componentes.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Habilita el cifrado y descifrado de búferes.                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](drm-programming-reference.md)
</dt> </dl>

 

 




