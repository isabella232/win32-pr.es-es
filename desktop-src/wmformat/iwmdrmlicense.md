---
title: Interfaz IWMDRMLicense
description: La interfaz IWMDRMLicense representa una lista de una o varias licencias.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- IWMDRMLicense interface windows Media Format
- Interfaz IWMDRMLicense windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38aadbda7a0ab6e899e4100adb5ff03873a4dd683fcb8f5893c506033545d558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847132"
---
# <a name="iwmdrmlicense-interface"></a>Interfaz IWMDRMLicense

La **interfaz IWMDRMLicense** representa una lista de una o varias licencias.

## <a name="members"></a>Miembros

La **interfaz IWMDRMLicense** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMLicense** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMLicense** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | Consulta si la licencia se puede conservar en un almacén de licencias local.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Crea un objeto descifrador mediante la configuración de la licencia actual.<br/>                                                                                                                                                   |
| [**CreateEncryptor**](iwmdrmlicense-createencryptor.md)                                 | Crea un objeto de cifrado mediante la configuración de la licencia actual.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Recupera todas las restricciones de vídeo análogo establecidas en la licencia actual.<br/>                                                                                                                                                     |
| [**GetInclusionList**](iwmdrmlicense-getinclusionlist.md)                               | Recupera toda la lista de inclusión de la cadena de licencias o licencia actual.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Recupera la licencia como datos lenguaje de marcado extensible (XML) o Extensible Media Rights (XMR).<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | Recupera una propiedad de la licencia actual.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Carga la información sobre la siguiente licencia de la lista.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Recupera información sobre todos los niveles de protección de salida (OPL) asignados a la licencia.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Guarda la licencia actual del almacén temporal en el almacén de licencias local permanente.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Restablece la lista de licencias a su estado original.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

