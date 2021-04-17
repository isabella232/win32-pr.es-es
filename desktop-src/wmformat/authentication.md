---
title: Autenticación (Windows Media Format 11 SDK)
description: Autenticación
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- SDK de Windows Media Format, autenticación
- SDK de Windows Media Format, autenticación de red
- Advanced Systems Format (ASF), autenticación
- ASF (formato de sistemas avanzados), autenticación
- Advanced Systems Format (ASF), autenticación de red
- ASF (formato de sistemas avanzados), autenticación de red
- autenticación
- autenticación de red, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bf815881ac7beb354fffbfdb9b5475d040e9e83
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105705111"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Autenticación (Windows Media Format 11 SDK)

El objeto lector puede controlar los desafíos de autenticación de red, incluida la autenticación implícita y la autenticación NTLM. En algunos casos, la aplicación debe proporcionar las credenciales del usuario a través de una interfaz de devolución de llamada:

-   Autenticación implícita: la aplicación debe implementar la interfaz **IWMCredentialCallback** , tal y como se describe más adelante en este tema.
-   Autenticación NTLM: el lector responde automáticamente con las credenciales de inicio de sesión del usuario. Si el usuario actual está autorizado para iniciar sesión en el servidor, la aplicación no tiene que hacer nada. Si el usuario no tiene autorización, la aplicación debe implementar la interfaz **IWMCredentialCallback** .

    > [!Note]  
    > Windows Media Services versión 4,1 no admite la autenticación NTLM a través de un servidor proxy. La autenticación NTLM requiere varios intercambios de cliente-servidor en la misma conexión y la versión 4,1 no mantiene una conexión persistente con el proxy. Windows Media Services 9 series en Microsoft Windows Server 2003 admite la autenticación NTLM a través de un servidor proxy, siempre y cuando el proxy admita conexiones persistentes.

     

Como se indicó, en algunos casos, la aplicación debe proporcionar las credenciales del usuario. Esto sucede a través de la interfaz **IWMCredentialCallback** , que tiene un único método, **AcquireCredentials**. Para admitir la autenticación, implemente esta interfaz en la aplicación. El objeto lector consulta esta interfaz llamando a **QueryInterface** en el puntero [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) que recibió de la aplicación en el método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) . Si el objeto lector necesita obtener las credenciales del usuario, llama al método **AcquireCredentials** de la aplicación.

Si las credenciales se van a enviar a través de la red sin cifrado, el lector establece la \_ \_ marca de texto no cifrado de credenciales WMT \_ en el parámetro *pdwFlags* . Esto permite a la aplicación advertir al usuario de que sus credenciales se enviarán en texto sin formato.

De lo contrario, el objeto lector cifra automáticamente las credenciales antes de enviarlas a través de la red. La aplicación puede devolverlos al objeto lector en texto sin formato. Además, si el objeto de lector establece la \_ marca de cifrado de credenciales WMT \_ , significa que el lector admite la obtención de credenciales cifradas de la aplicación. En ese caso, la aplicación puede devolver las credenciales en texto sin formato, o bien cifrarlas mediante la función **CryptProtectData** , que se describe en la documentación del SDK de la plataforma. Si la aplicación cifra las credenciales, debe establecer la \_ \_ marca de cifrado de credenciales WMT en el parámetro *pdwFlags* antes de que el método devuelva.

Por lo general, no es necesario cifrar los datos, porque el objeto lector los cifra si es necesario. Sin embargo, el cifrado puede ser útil si la aplicación mantiene el nombre de usuario y la contraseña en la memoria, ya que impide que un atacante inspeccione un volcado de memoria del proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




