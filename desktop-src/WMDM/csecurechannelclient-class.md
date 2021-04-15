---
title: Clase CSecureChannelClient
description: Clase CSecureChannelClient
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Administrador de dispositivos, clase CSecureChannelClient
- Administrador de dispositivos, clase CSecureChannelClient
- aplicaciones de escritorio, clase CSecureChannelClient
- referencia de programación, clase CSecureChannelClient
- referencia de Windows Media Administrador de dispositivos, clase CSecureChannelClient
- Clase CSecureChannelClient
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695634"
---
# <a name="csecurechannelclient-class"></a>Clase CSecureChannelClient

La clase **CSecureChannelClient** es una clase auxiliar (no una interfaz) que permite a las aplicaciones autenticarse, cifrar y descifrar datos, y crear equipos Mac.

La clase **CSecureChannelClient** expone los métodos siguientes.



| Método                                                            | Descripción                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Authenticate**](/previous-versions/ms983906(v=msdn.10))         | Desencadena el intercambio de certificados entre componentes para establecer la confianza.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Descifra los datos recibidos a través de un parámetro.                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Cifra los datos que se envían a través de un parámetro.                                                                         |
| [**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10)) | Comprueba que se ha establecido correctamente un canal de autenticación seguro. Las aplicaciones no usan este método. |
| [**GetAppSec**](/previous-versions/ms868498(v=msdn.10))               | Recupera los niveles de seguridad de la aplicación de los componentes locales y remotos.                                             |
| [**GetSessionKey**](/previous-versions/bb231590(v=vs.85))       | Recupera la clave de sesión actual. Las aplicaciones no usan este método.                                               |
| [**MACFinal**](/previous-versions/bb231591(v=vs.85))                 | Libera el canal de código de autenticación de mensajes (MAC) y recupera un valor de MAC final.                                   |
| [**MACInit**](/previous-versions/bb231592(v=vs.85))                   | Adquiere un canal de código de autenticación de mensajes (MAC).                                                                     |
| [**MACUpdate**](/previous-versions/bb231593(v=vs.85))               | Agrega un valor a un código de autenticación de mensajes (MAC).                                                                      |
| [**SetCertificate**](/previous-versions/ms868504(v=msdn.10))     | Especifica el certificado y la clave privada del cliente de canal autenticado seguro (SAC).                               |
| [**SetInterface**](/previous-versions/bb231595(v=vs.85))         | Selecciona la interfaz que se usa para las comunicaciones de canal autenticado seguro (SAC).                                         |
| [**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))       | Establece la clave de sesión que se usa para comunicarse con otro componente. Las aplicaciones no usan este método.         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Clase CSecureChannelServer**](csecurechannelserver-class.md)
</dt> <dt>

[**Interfaz IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> </dl>

 

 