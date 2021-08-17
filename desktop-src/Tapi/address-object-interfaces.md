---
description: Los objetos de dirección son entidades que pueden realizar o recibir llamadas. Las interfaces y los métodos relacionados permiten a una aplicación obtener y establecer información sobre una dirección, como si la dirección tiene compatibilidad con el identificador de autor de la llamada.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Interfaces de objeto de dirección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2254ba47e81ebd40f5ce95a1c870c363d09243c69cec0c4ec358cf3ee5604de7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949189"
---
# <a name="address-object-interfaces"></a>Interfaces de objeto de dirección

[Los objetos de](address-object.md) dirección son entidades que pueden realizar o recibir llamadas. Las interfaces y los métodos relacionados permiten a una aplicación obtener y establecer información sobre una dirección, como si la dirección tiene compatibilidad con el identificador de autor de la llamada.

Las interfaces [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**ITForwardInformation,**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation) [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)e [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) no se exponen directamente en el objeto Address, pero están estrechamente relacionadas con él y se enumeran aquí para mayor comodidad de referencia.



| Interfaz                                                            | Descripción                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Actúa como interfaz base para el objeto Address.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Deriva de [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress); proporciona métodos adicionales que admiten dispositivos telefónicos.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Obtiene información sobre las funcionalidades de una dirección.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Proporciona información sobre los eventos de dirección.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Realiza la traducción de direcciones.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Obtiene información de traducción de direcciones.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Proporciona métodos para recuperar información de tarjeta de llamada.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Proporciona métodos para configurar e implementar el reenvío de llamadas.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Admite aplicaciones heredadas que requieren acceso directo a un dispositivo y su configuración.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Extiende [**ITLegacyAddressMediaControl al**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) permitir la configuración de parámetros relacionados con dispositivos de línea. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Obtiene información relacionada con la ubicación de la parte que realiza la llamada.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Obtiene información sobre las funcionalidades de soporte multimedia de una dirección.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Obtiene información sobre los terminales disponibles y proporciona un método para crear terminales adicionales.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Enumera [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Enumera [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Si la dirección es una dirección [MSP de Wave,](wave-msp.md) la interfaz [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) también se expone en el objeto Address.

 

 
