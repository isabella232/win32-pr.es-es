---
title: Interfaz IWMDRMNonSilentLicenseAquisition
description: La interfaz IWMDRMNonSilentLicenseAquisition proporciona métodos que permiten la adquisición de licencias que requieren la intervención del usuario. Esta interfaz se puede obtener mediante la adquisición de licencias no silenciosas.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- IWMDRMNonSilentLicenseAquisition interface windows Media Format
- IWMDRMNonSilentLicenseAquisition interface windows Media Format , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247268"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interfaz IWMDRMNonSilentLicenseAquisition

La **interfaz IWMDRMNonSilentLicenseAquisition** proporciona métodos que permiten la adquisición de licencias que requieren la intervención del usuario.

Esta interfaz se puede obtener mediante la adquisición de licencias no silenciosas. Después de llamar [**a IWMDRMLicenseManagement::AcquireLicense,**](iwmdrmlicensemanagement-acquirelicense.md) se generará un evento **MEWMDRMRMLicenseAcquisitionCompleted.** Llame al **método IMFMediaEvent::GetValue** del evento para obtener un puntero a una **interfaz IUnknown** que se puede consultar para un puntero a una instancia de esta interfaz.

## <a name="members"></a>Members

La **interfaz IWMDRMNonSilentLicenseAquisition** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNonSilentLicenseAquisition** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMNonSilentLicenseAquisition** tiene estos métodos.



| Método                                                                | Descripción                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Recupera el desafío de licencia que se debe publicar en el servidor de licencias.<br/> |
| [**Geturl**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Recupera la dirección URL en la que se debe publicar el desafío de licencia.<br/>           |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Adquisición de licencias no silenciosas**](non-silent-license-acquisition.md)
</dt> </dl>

 

