---
title: Interfaz IWMDRMNetTransmitter
description: La interfaz IWMDRMNetTransmitter proporciona métodos necesarios para usar Windows DRM multimedia para dispositivos de red como transmisor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase IID \_ IWMDRMNetTransmitter como parámetro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- IWMDRMNetTransmitter interface windows Media Format
- IWMDRMNetTransmitter interface windows Media Format , descrito
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247281"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interfaz IWMDRMNetTransmitter

La **interfaz IWMDRMNetTransmitter proporciona** métodos necesarios para usar Windows DRM multimedia para dispositivos de red como transmisor.

Para obtener una instancia de esta interfaz, llame [**a IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Pase **IID \_ IWMDRMNetTransmitter como** parámetro *riid.*

## <a name="members"></a>Members

La **interfaz IWMDRMNetTransmitter** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNetTransmitter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMNetTransmitter** tiene estos métodos.



| Método                                                                        | Descripción                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Genera un mensaje de respuesta de licencia hoja.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Genera un mensaje de respuesta de licencia raíz<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Procesa un desafío de licencia enviado por un receptor Windows DRM multimedia de Microsoft para dispositivos de red<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Interfaz IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

