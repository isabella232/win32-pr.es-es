---
title: Interfaces de cliente DRM de Microsoft Windows Media
description: Interfaces de cliente DRM de Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- SDK de Windows Media Format, interfaces
- Administración de derechos digitales (DRM), interfaces
- DRM (administración de derechos digitales), interfaces
- API extendidas del cliente DRM, interfaces
- API extendidas del cliente, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421774"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Interfaces de cliente DRM de Microsoft Windows Media

En la tabla siguiente se describen las interfaces compatibles con las API de cliente de Windows Media DRM.



| Interfaz                                                                    | Descripción                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Proporciona la definición de una devolución de llamada de estado que se puede implementar para controlar las operaciones DRM asincrónicas.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Proporciona un método para descifrar el contenido.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Proporciona un método para cifrar los datos en su lugar.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Cifra los datos de bloques no contiguos.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Extensión de la interfaz **IMFMediaEventGenerator** que proporciona un método para cancelar las operaciones asincrónicas. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Habilita la recuperación de información de estado avanzada sobre el progreso de la individualización.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Representa una o más licencias en el almacén de licencias local.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Habilita la recuperación de información de estado detallada sobre una operación de copia de seguridad o restauración de licencias.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Habilita las operaciones de administración para el almacén de licencias local.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Proporciona opciones de administración adicionales para el almacén de licencias local.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Permite que las aplicaciones consulten los derechos y el estado de la licencia de un archivo protegido.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | Proporciona los métodos necesarios para crear una aplicación DRM de Microsoft Windows Media para el receptor de dispositivos de red.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | Proporciona los métodos necesarios para crear una aplicación DRM de Microsoft Windows Media para el transmisor de dispositivos de red.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Proporciona métodos que permiten la adquisición de licencias con la intervención del usuario.                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | Crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Administra varios procesos relacionados con la seguridad para el equipo cliente y el subsistema DRM.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Administra la revocación y renovación de componentes.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Habilita el cifrado y descifrado de los búferes.                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación**](drm-programming-reference.md)
</dt> </dl>

 

 




