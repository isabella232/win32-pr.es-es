---
title: Interfaz IWMDRMSecurity
description: La interfaz IWMDRMSecurity administra una gran variedad de información relacionada con la seguridad para el equipo cliente y el subsistema de administración de derechos digitales (DRM). Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Interfaz IWMDRMSecurity formato de Windows Media
- Interfaz IWMDRMSecurity formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358178"
---
# <a name="iwmdrmsecurity-interface"></a>Interfaz IWMDRMSecurity

La interfaz **IWMDRMSecurity** administra una gran variedad de información relacionada con la seguridad para el equipo cliente y el subsistema de administración de derechos digitales (DRM).

Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Pase el **IID \_ IWMDRMSecurity** como parámetro *riid* .

## <a name="members"></a>Miembros

La interfaz **IWMDRMSecurity** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMSecurity** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Determina si se ha revocado un certificado.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Recupera interfaces del habilitador de contenido que habilita la renovación de componentes basándose en certificados revocados.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Recupera interfaces del habilitador de contenido que habilita la renovación de componentes basándose en certificados hash.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Recupera el certificado de equipo del subsistema DRM en el equipo cliente.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Recupera una lista de revocación de certificados del almacén local.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Recupera el número de versión de una lista de revocación de certificados en el almacén local.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Recupera la versión del subsistema DRM en el equipo cliente.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Inicia una actualización de seguridad para el subsistema DRM en el equipo cliente.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Establece una lista de revocación de certificados en el almacén local.<br/>                                                |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





