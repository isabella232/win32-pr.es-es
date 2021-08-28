---
title: IWMDRMLicenseManagement (interfaz)
description: La interfaz IWMDRMLicenseManagement proporciona métodos que realizan operaciones generales relacionadas con el almacén de licencias local. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase IID \_ IWMDRMLicenseManagement como parámetro riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- IWMDRMLicenseManagement interface windows Media Format
- IWMDRMLicenseManagement interface windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63baeeb46baa877ccc294d1136351ec123d6c4661ee73d548b62d8cb4db05734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027553"
---
# <a name="iwmdrmlicensemanagement-interface"></a>IWMDRMLicenseManagement (interfaz)

La **interfaz IWMDRMLicenseManagement proporciona** métodos que realizan operaciones generales relacionadas con el almacén de licencias local.

Para obtener una instancia de esta interfaz, llame [**a IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Pase **IID \_ IWMDRMLicenseManagement** como *parámetro riid.*

## <a name="members"></a>Miembros

La **interfaz IWMDRMLicenseManagement** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMLicenseManagement** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMLicenseManagement** tiene estos métodos.



| Método                                                                                               | Descripción                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Adquiere de forma asincrónica una licencia de una dirección URL especificada.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Crea una copia de seguridad de las licencias en el almacén de licencias local.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Quita las licencias marcadas del almacén de licencias y desfragmenta el almacén para mejorar el rendimiento.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Crea un objeto enumerador de licencias rellenado con información de licencia basada en valores de parámetro.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Genera un desafío de revocación de licencias.<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Elimina una licencia del almacén de licencias local temporal.<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Inicia la supervisión de un proceso de adquisición de licencias.<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Elimina una licencia que se importó para el contenido protegido originalmente con otro sistema de protección de contenido.<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Revoca las licencias del almacén de licencias local.<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Restaura las licencias de las que se ha vuelto a hacer una copia de seguridad.<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Agrega una licencia al almacén de licencias local.<br/>                                                                   |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





