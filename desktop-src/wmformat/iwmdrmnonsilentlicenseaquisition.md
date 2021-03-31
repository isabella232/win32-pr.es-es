---
title: Interfaz IWMDRMNonSilentLicenseAquisition
description: La interfaz IWMDRMNonSilentLicenseAquisition proporciona métodos que permiten adquirir licencias que requieren la intervención del usuario. Esta interfaz se puede obtener realizando una adquisición de licencias no silenciosa.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media
- Interfaz IWMDRMNonSilentLicenseAquisition formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792682"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interfaz IWMDRMNonSilentLicenseAquisition

La interfaz **IWMDRMNonSilentLicenseAquisition** proporciona métodos que permiten adquirir licencias que requieren la intervención del usuario.

Esta interfaz se puede obtener realizando una adquisición de licencias no silenciosa. Después de llamar a [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , se generará un evento **MEWMDRMLicenseAcquisitionCompleted** . Llame al método **IMFMediaEvent:: GetValue** del evento para obtener un puntero a una interfaz **IUnknown** que se puede consultar para un puntero a una instancia de esta interfaz.

## <a name="members"></a>Miembros

La interfaz **IWMDRMNonSilentLicenseAquisition** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNonSilentLicenseAquisition** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMNonSilentLicenseAquisition** tiene estos métodos.



| Método                                                                | Descripción                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Recupera el desafío de la licencia que debe publicarse en el servidor de licencias.<br/> |
| [**GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Recupera la dirección URL a la que se debe publicar el desafío de licencia.<br/>           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Adquisición de licencias no silenciosa**](non-silent-license-acquisition.md)
</dt> </dl>

 

