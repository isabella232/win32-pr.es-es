---
title: Autenticación (Windows SDK de formato multimedia 11)
description: Authentication
ms.assetid: 9c181615-e864-4588-846f-d04d73824f5f
keywords:
- Windows SDK de formato multimedia, autenticación
- Windows SDK de formato multimedia, autenticación de red
- Formato de sistemas avanzados (ASF), autenticación
- ASF (formato de sistemas avanzados), autenticación
- Formato de sistemas avanzados (ASF), autenticación de red
- ASF (formato de sistemas avanzados), autenticación de red
- autenticación
- autenticación de red, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee276bc2800ad7f2d5fa94f00e282dc7d4f5402396d69eb7e3b240fd4303f4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007125"
---
# <a name="authentication-windows-media-format-11-sdk"></a>Autenticación (Windows SDK de formato multimedia 11)

El objeto lector puede controlar los desafíos de autenticación de red, incluida la autenticación implícita y la autenticación NTLM. En algunos casos, la aplicación debe proporcionar las credenciales del usuario a través de una interfaz de devolución de llamada:

-   Autenticación implícita: la aplicación debe implementar la **interfaz IWMCredentialCallback,** como se describe más adelante en este tema.
-   Autenticación NTLM: el lector responde automáticamente con las credenciales de inicio de sesión del usuario. Si el usuario actual está autorizado para iniciar sesión en el servidor, la aplicación no tiene que hacer nada. Si el usuario no tiene autorización, la aplicación debe implementar la **interfaz IWMCredentialCallback.**

    > [!Note]  
    > Servicios de Windows Media versión 4.1 no admite la autenticación NTLM a través de un servidor proxy. La autenticación NTLM requiere varios intercambios cliente-servidor en la misma conexión y la versión 4.1 no mantiene una conexión persistente con el proxy. Servicios de Windows Media serie 9 de Microsoft Windows Server 2003 admite la autenticación NTLM a través de un servidor proxy, siempre y cuando el proxy admita conexiones de conexión continua.

     

Como se indicó, en algunos casos la aplicación debe proporcionar las credenciales del usuario. Esto sucede a través de la **interfaz IWMCredentialCallback,** que tiene un único método, **AcquireCredentials**. Para admitir la autenticación, implemente esta interfaz en la aplicación. El objeto reader consulta esta interfaz llamando a **QueryInterface** en el [**puntero IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) que recibió de la aplicación en el [**método IWMReader::Open.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) Si el objeto de lector necesita obtener las credenciales del usuario, llama al método **AcquireCredentials de la** aplicación.

Si las credenciales se enviarán a través de la red sin cifrado, el lector establece la marca WMT CREDENTIAL CLEAR TEXT en el \_ \_ parámetro \_ *pdwFlags.* Esto ofrece a la aplicación la oportunidad de advertir al usuario de que sus credenciales se enviarán en texto sin formato.

De lo contrario, el objeto lector cifra automáticamente las credenciales antes de enviarlas a través de la red. La aplicación puede devolverlos al objeto lector en texto sin formato. Además, si el objeto de lector establece la marca WMT CREDENTIAL ENCRYPT, significa que el lector admite la obtención de credenciales cifradas \_ \_ de la aplicación. En ese caso, la aplicación puede devolver las credenciales en texto sin formato o cifrarlas a sí misma mediante la función **CryptProtectData,** que se describe en la documentación del SDK de plataforma. Si la aplicación cifra las credenciales, debe establecer la marca WMT CREDENTIAL ENCRYPT en el \_ \_ parámetro *pdwFlags* antes de que el método vuelva.

Por lo general, no es necesario cifrar los datos, ya que el objeto lector cifra los datos si es necesario. Sin embargo, el cifrado puede ser útil si la aplicación mantiene el nombre de usuario y la contraseña en memoria, ya que impide que un atacante inspeccione un volcado de memoria del proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMCredentialCallback (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)
</dt> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> </dl>

 

 




