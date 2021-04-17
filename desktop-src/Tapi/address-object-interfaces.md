---
description: Los objetos de dirección son entidades que pueden realizar o recibir llamadas. Las interfaces y los métodos relacionados permiten a una aplicación obtener y establecer información relativa a una dirección, como, por ejemplo, si la dirección tiene compatibilidad con el identificador del llamador.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Interfaces del objeto Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef19db02123e10e839906a00931ef246d19d2c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687898"
---
# <a name="address-object-interfaces"></a>Interfaces del objeto Address

Los [objetos de dirección](address-object.md) son entidades que pueden realizar o recibir llamadas. Las interfaces y los métodos relacionados permiten a una aplicación obtener y establecer información relativa a una dirección, como, por ejemplo, si la dirección tiene compatibilidad con el identificador del llamador.

Las interfaces [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation), [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)y [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) no se exponen directamente en el objeto address, pero están estrechamente relacionadas con ella y se enumeran aquí para mayor comodidad de referencia.



| Interfaz                                                            | Descripción                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Actúa como interfaz base para el objeto Address.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Deriva de [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress); proporciona métodos adicionales que admiten dispositivos telefónicos.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Obtiene información sobre las funciones de una dirección.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Proporciona información sobre los eventos de dirección.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Realiza la traducción de direcciones.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Obtiene la información de traducción de direcciones.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Proporciona métodos para recuperar información de la tarjeta de llamada.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Proporciona métodos para configurar e implementar el reenvío de llamadas.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Es compatible con aplicaciones heredadas que requieren acceso directo a un dispositivo y a su configuración.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Extiende [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) permitiendo la configuración de parámetros relacionados con los dispositivos de línea. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Obtiene información relacionada con la ubicación de la entidad que realiza la llamada.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Obtiene información relativa a las capacidades de soporte de multimedia de una dirección.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Obtiene información sobre los terminales disponibles y proporciona un método para crear terminales adicionales.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Enumera [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress).                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Enumera [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard).                                                                                              |



 

Si la dirección es una dirección de [onda MSP](wave-msp.md) , la interfaz [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) también se expone en el objeto Address.

 

 
