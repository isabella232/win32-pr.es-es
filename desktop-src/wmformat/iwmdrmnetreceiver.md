---
title: Interfaz IWMDRMNetReceiver
description: La interfaz IWMDRMNetReceiver proporciona los métodos necesarios para usar DRM de Microsoft Windows Media para dispositivos de red como receptor. Para obtener una instancia de esta interfaz, llame a IWMDRMProvider CreateObject. Pase \_ el IID IWMDRMNetReceiver como parámetro riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Interfaz IWMDRMNetReceiver formato de Windows Media
- Interfaz IWMDRMNetReceiver formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a85ae1525a81e97984e29a5dd28763d934dba2b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419733"
---
# <a name="iwmdrmnetreceiver-interface"></a>Interfaz IWMDRMNetReceiver

La interfaz **IWMDRMNetReceiver** proporciona los métodos necesarios para usar DRM de Microsoft Windows Media para dispositivos de red como receptor.

Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Pase el **IID \_ IWMDRMNetReceiver** como parámetro *riid* .

## <a name="members"></a>Miembros

La interfaz **IWMDRMNetReceiver** hereda de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMNetReceiver** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMNetReceiver** tiene estos métodos.



| Método                                                                               | Descripción                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Genera un desafío de licencia que se envía al transmisor al solicitar contenido protegido.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Genera un desafío de registro que se envía al transmisor cuando el receptor se registra o se vuelve a validar.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Procesa la respuesta de la licencia enviada por el transmisor en respuesta a un desafío de licencia.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Procesa la respuesta de registro enviada por el transmisor en respuesta a un desafío de registro.<br/>                    |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**Interfaz IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





