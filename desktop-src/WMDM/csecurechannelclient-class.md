---
title: CSecureChannelClient (clase)
description: CSecureChannelClient (clase)
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Windows Media Administrador de dispositivos,CSecureChannelClient (clase)
- Administrador de dispositivos,CSecureChannelClient (clase)
- aplicaciones de escritorio, clase CSecureChannelClient
- referencia de programación, clase CSecureChannelClient
- referencia de Windows Media Administrador de dispositivos,CSecureChannelClient (clase)
- CSecureChannelClient (clase)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ef469c1e7a73b04124850952ef0690bd18c82ecb3fc624d08df081b7b669637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585618"
---
# <a name="csecurechannelclient-class"></a>CSecureChannelClient (clase)

La **clase CSecureChannelClient** es una clase auxiliar (no una interfaz) que permite a las aplicaciones autenticarse, cifrar y descifrar datos y crear MAC.

La **clase CSecureChannelClient** expone los métodos siguientes.



| Método                                                            | Descripción                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Autenticar**](/previous-versions/ms983906(v=msdn.10))         | Desencadena el intercambio de certificados entre componentes para establecer confianza.                                              |
| [**DecryptParam**](/previous-versions/bb231586(v=vs.85))         | Descifra los datos recibidos a través de un parámetro .                                                                               |
| [**EncryptParam**](/previous-versions/bb231587(v=vs.85))         | Cifra los datos que se envían a través de un parámetro .                                                                         |
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

[**CSecureChannelServer (clase)**](csecurechannelserver-class.md)
</dt> <dt>

[**IComponentAuthenticate (interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> </dl>

 

 