---
title: Interfaz IWMDRMLicenseManagement
description: La interfaz IWMDRMLicenseManagement proporciona métodos que realizan operaciones generales relacionadas con el almacén de licencias local. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase \_ el IID IWMDRMLicenseManagement como parámetro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Interfaz IWMDRMLicenseManagement formato de Windows Media
- Interfaz IWMDRMLicenseManagement formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358087"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Interfaz IWMDRMLicenseManagement

La interfaz **IWMDRMLicenseManagement** proporciona métodos que realizan operaciones generales relacionadas con el almacén de licencias local.

Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Pase el **IID \_ IWMDRMLicenseManagement** como parámetro *riid* .

## <a name="members"></a>Miembros

La interfaz **IWMDRMLicenseManagement** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMLicenseManagement** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMLicenseManagement** tiene estos métodos.



| Método                                                                                               | Descripción                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Adquiere de forma asincrónica una licencia de una dirección URL especificada.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Crea una copia de seguridad de las licencias en el almacén de licencias local.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Quita las licencias marcadas del almacén de licencias y desfragmenta el almacén para mejorar el rendimiento.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Crea un objeto de enumerador de licencia rellenado con información de licencia basada en valores de parámetro.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Genera un desafío de revocación de licencia.<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Elimina una licencia del almacén de licencias local temporal.<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Inicia la supervisión de un proceso de adquisición de licencias.<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Revoca las licencias del almacén de licencias local.<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Restaura las licencias de las que se realizó previamente una copia de seguridad.<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Agrega una licencia al almacén de licencias local.<br/>                                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





