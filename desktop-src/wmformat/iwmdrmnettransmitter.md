---
title: Interfaz IWMDRMNetTransmitter
description: La interfaz IWMDRMNetTransmitter proporciona los métodos necesarios para usar DRM de Windows Media para dispositivos de red como transmisor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase \_ el IID IWMDRMNetTransmitter como parámetro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Interfaz IWMDRMNetTransmitter formato de Windows Media
- Interfaz IWMDRMNetTransmitter formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359180"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interfaz IWMDRMNetTransmitter

La interfaz **IWMDRMNetTransmitter** proporciona los métodos necesarios para usar DRM de Windows Media para dispositivos de red como transmisor.

Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Pase el **IID \_ IWMDRMNetTransmitter** como parámetro *riid* .

## <a name="members"></a>Miembros

La interfaz **IWMDRMNetTransmitter** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNetTransmitter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMNetTransmitter** tiene estos métodos.



| Método                                                                        | Descripción                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Genera un mensaje de respuesta de licencia de hoja.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Genera un mensaje de respuesta de licencia raíz<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Procesa un desafío de licencia enviado por un receptor de Microsoft Windows Media DRM para dispositivos de red<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

