---
title: IWMDRMNetReceiver (interfaz)
description: La interfaz IWMDRMNetReceiver proporciona los métodos necesarios para usar Microsoft Windows Media DRM para dispositivos de red como receptor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase IID \_ IWMDRMNetReceiver como parámetro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- IWMDRMNetReceiver interface windows Media Format
- IWMDRMNetReceiver interface windows Media Format , descrito
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb917d7d229b81a6792461c506b2a6b50aaee2af3bd5f133e44273077924f86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930115"
---
# <a name="iwmdrmnetreceiver-interface"></a>IWMDRMNetReceiver (interfaz)

La **interfaz IWMDRMNetReceiver** proporciona los métodos necesarios para usar Microsoft Windows Media DRM para dispositivos de red como receptor.

Para obtener una instancia de esta interfaz, llame [**a IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md). Pase **IID \_ IWMDRMNetReceiver como** parámetro *riid.*

## <a name="members"></a>Miembros

La **interfaz IWMDRMNetReceiver** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMNetReceiver** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMNetReceiver** tiene estos métodos.



| Método                                                                               | Descripción                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Genera un desafío de licencia que se envía al transmisor al solicitar contenido protegido.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Genera un desafío de registro que se envía al transmisor cuando el receptor se registra o se vuelve a validar.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Procesa la respuesta de licencia enviada por el transmisor en respuesta a un desafío de licencia.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Procesa la respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.<br/>                    |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**IWMDRMNetTransmitter (interfaz)**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





