---
title: Interfaz IWMDRMNetTransmitter
description: La interfaz IWMDRMNetTransmitter proporciona métodos necesarios para usar Windows DRM multimedia para dispositivos de red como transmisor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase IID \_ IWMDRMNetTransmitter como parámetro riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- IWMDRMNetTransmitter interface windows Media Format
- Interfaz IWMDRMNetTransmitter windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7526ad349403abdb74f1e5684356af1b51b91f99b40e8e26a3b04932d4e5cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027563"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interfaz IWMDRMNetTransmitter

La **interfaz IWMDRMNetTransmitter** proporciona métodos necesarios para usar drm Windows multimedia para dispositivos de red como transmisor.

Para obtener una instancia de esta interfaz, llame [**a IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Pase **IID \_ IWMDRMNetTransmitter como** parámetro *riid.*

## <a name="members"></a>Miembros

La **interfaz IWMDRMNetTransmitter** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMDRMNetTransmitter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMNetTransmitter** tiene estos métodos.



| Método                                                                        | Descripción                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Genera un mensaje de respuesta de licencia hoja.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Genera un mensaje de respuesta de licencia raíz<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | Procesa un desafío de licencia enviado por un receptor de DRM Windows Multimedia de Microsoft para dispositivos de red<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMNetReceiver (interfaz)**](iwmdrmnetreceiver.md)
</dt> </dl>

 

