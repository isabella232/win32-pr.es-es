---
title: CSecureChannelServer (clase)
description: CSecureChannelServer (clase)
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Windows Media Administrador de dispositivos,CSecureChannelServer (clase)
- Administrador de dispositivos,CSecureChannelServer (clase)
- service providers,CSecureChannelServer (clase)
- referencia de programación, clase CSecureChannelServer
- referencia de Windows Media Administrador de dispositivos,CSecureChannelServer (clase)
- CSecureChannelServer (clase)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87627fcdee6da42927ab88411dd579225dc38f025ae73bf9f4fe787c0c5e44bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585489"
---
# <a name="csecurechannelserver-class"></a>CSecureChannelServer (clase)

La **clase CSecureChannelServer** es una clase auxiliar (no una interfaz) que permite a un proveedor de servicios o a un proveedor de contenido seguro autenticar una aplicación mediante la interfaz [**IComponentAuthenticate,**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) cifrar y descifrar datos, y crear firmas MAC. El proceso de autenticación requiere que la aplicación cree **un objeto CSecureChannelClient** y que el proveedor de servicios cree un **objeto CSecureChannelServer.** Las **clases CSecureChannelClient** y **CSecureChannelServer** se declaran en la biblioteca de vínculos estáticos, Mssachlp.lib. Todos los métodos de Windows media Administrador de dispositivos, proveedor de servicios e interfaces de proveedor de contenido seguro pueden devolver WMDM E NOTCERTIFIED para indicar que el autor de la llamada no se ha autenticado \_ \_ correctamente.

La **clase CSecureChannelServer** expone los métodos siguientes.



| Método                                                            | Descripción                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**DecryptParam**](/previous-versions/bb231598(v=vs.85))         | Descifra los datos contenidos en un parámetro .                                                 |
| [**EncryptParam**](/previous-versions/ms868509(v=msdn.10))         | Cifra los datos contenidos en un parámetro .                                                 |
| [**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) | Comprueba que se ha establecido correctamente un canal de autenticación seguro.            |
| [**GetAppSec**](/previous-versions/bb231601(v=vs.85))               | Recupera los niveles de seguridad de la aplicación de los componentes locales y remotos.               |
| [**GetSessionKey**](/previous-versions/bb231602(v=vs.85))       | Recupera la clave de sesión actual.                                                          |
| [**MACFinal**](/previous-versions/ms868513(v=msdn.10))                 | Libera el canal de código de autenticación de mensajes (MAC) y recupera un valor de MAC final.     |
| [**MACInit**](/previous-versions/ms868514(v=msdn.10))                   | Adquiere un canal de código de autenticación de mensajes (MAC).                                       |
| [**MACUpdate**](/previous-versions/ms868515(v=msdn.10))               | Actualiza el valor del código de autenticación de mensajes (MAC) con un valor de parámetro.                 |
| [**SACAuth**](/previous-versions/ms868516(v=msdn.10))                   | Establece un canal autenticado seguro entre componentes.                              |
| [**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))   | Notifica los protocolos admitidos por un componente.                                             |
| [**SetCertificate**](/previous-versions/ms868518(v=msdn.10))     | Especifica el certificado y la clave privada del servidor de canal autenticado seguro (SAC). |
| [**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))       | Establece la clave de sesión que se usa para comunicarse con otro componente.                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CSecureChannelClient (clase)**](csecurechannelclient-class.md)
</dt> <dt>

[**IComponentAuthenticate (interfaz)**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[**Interfaces para proveedores de servicios**](interfaces-for-service-providers.md)
</dt> <dt>

[**Uso de canales autenticados seguros**](using-secure-authenticated-channels.md)
</dt> </dl>

 

 