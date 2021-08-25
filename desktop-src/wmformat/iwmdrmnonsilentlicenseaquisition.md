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
ms.openlocfilehash: c953588cb457e8afb21cca38e9daed08b2387ab9fb7871ecd6b17dae9dca152f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110355"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interfaz IWMDRMNonSilentLicenseAquisition

La **interfaz IWMDRMNonSilentLicenseAquisition** proporciona métodos que permiten la adquisición de licencias que requieren la intervención del usuario.

Esta interfaz se puede obtener mediante la adquisición de licencias no silenciosas. Después de llamar [**a IWMDRMLicenseManagement::AcquireLicense,**](iwmdrmlicensemanagement-acquirelicense.md) se generará un evento **MEWMDRMRMLicenseAcquisitionCompleted.** Llame al **método IMFMediaEvent::GetValue** del evento para obtener un puntero a una **interfaz IUnknown** que se puede consultar para un puntero a una instancia de esta interfaz.

## <a name="members"></a>Miembros

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

 

