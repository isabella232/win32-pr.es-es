---
title: Interfaz IWMDRMLicense
description: La interfaz IWMDRMLicense representa una lista de una o más licencias.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Interfaz IWMDRMLicense formato de Windows Media
- Interfaz IWMDRMLicense formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487951"
---
# <a name="iwmdrmlicense-interface"></a>Interfaz IWMDRMLicense

La interfaz **IWMDRMLicense** representa una lista de una o más licencias.

## <a name="members"></a>Miembros

La interfaz **IWMDRMLicense** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicense** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMLicense** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | Consulta si la licencia puede conservarse en un almacén de licencias local.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Crea un objeto descifrador con la configuración de la licencia actual.<br/>                                                                                                                                                   |
| [**CreateEncryptor**](iwmdrmlicense-createencryptor.md)                                 | Crea un objeto de sistema de cifrado con los valores de la licencia actual.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Recupera todas las restricciones de vídeo analógico establecidas en la licencia actual.<br/>                                                                                                                                                     |
| [**GetInclusionList**](iwmdrmlicense-getinclusionlist.md)                               | Recupera la lista de inclusión completa para la licencia actual o la cadena de licencias.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Recupera la licencia como lenguaje de marcado extensible (XML) o los datos de los derechos multimedia extensibles (XMR).<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | Recupera una propiedad de la licencia actual.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Carga la información sobre la siguiente licencia de la lista.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Recupera información sobre todos los niveles de protección de salida (OPLs) asignados a la licencia.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Restablece la lista de licencias a su estado original.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

