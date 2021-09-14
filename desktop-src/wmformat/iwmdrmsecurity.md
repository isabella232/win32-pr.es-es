---
title: Interfaz IWMDRMSecurity
description: La interfaz IWMDRMSecurity administra una variedad de información relacionada con la seguridad para el equipo cliente y el subsistema de administración de derechos digitales (DRM). Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- IWMDRMSecurity interface windows Media Format
- IWMDRMSecurity interface windows Media Format , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256238"
---
# <a name="iwmdrmsecurity-interface"></a>Interfaz IWMDRMSecurity

La **interfaz IWMDRMSecurity** administra una variedad de información relacionada con la seguridad para el equipo cliente y el subsistema de administración de derechos digitales (DRM).

Para obtener una instancia de esta interfaz, llame [**a IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Pase **IID \_ IWMDRMSecurity como** parámetro *riid.*

## <a name="members"></a>Members

La **interfaz IWMDRMSecurity** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMSecurity** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Determina si se ha revocado un certificado.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Recupera las interfaces del habilitador de contenido que permiten la renovación de componentes en función de los certificados revocados.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Recupera las interfaces del habilitador de contenido que permiten la renovación de componentes basados en certificados con hash.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Recupera el certificado de máquina del subsistema DRM en el equipo cliente.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Recupera una lista de revocación de certificados del almacén local.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Recupera el número de versión de una lista de revocación de certificados en el almacén local.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Recupera la versión del subsistema DRM en el equipo cliente.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Inicia una actualización de seguridad en el subsistema DRM en el equipo cliente.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Establece una lista de revocación de certificados en el almacén local.<br/>                                                |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Ejemplo de individualización de DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





