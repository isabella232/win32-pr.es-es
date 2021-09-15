---
description: En este tema se describe el contenido de vídeo&\# 8211;funcionalidades de protección que un controlador de gráficos puede proporcionar.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based Content Protection con D3D11 Video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24af51187c400c11afa2ea273e7718c2d38ce429
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475836"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based Content Protection con D3D11 Video

En este tema se describen las funcionalidades de protección de contenido de vídeo que puede proporcionar un controlador de gráficos.

-   [Introducción](#introduction)
-   [Información general del proceso de descodización](#overview-of-the-decoding-process)
-   [Cifrado de búferes de vídeo comprimidos para el descodificador](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Consultar las Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Configurar el canal autenticado](#2-configure-the-authenticated-channel)
    -   [3. Configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
    -   [4. Asociación del descodificador a la sesión criptográfica](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Envío de comandos de canal autenticados](#sending-authenticated-channel-commands)
-   [Envío de consultas de canal autenticadas](#sending-authenticated-channel-queries)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En el diagrama siguiente se muestra una vista simplificada de cómo viaja el contenido de vídeo protegido a través de la canalización que se va a representar.

![diagrama que muestra el contenido de vídeo protegido.](images/d3d9video01.png)

> [!Note]
>
> La [ruta de acceso multimedia](protected-media-path.md) protegida (PMP) no se muestra en este diagrama. El flujo de datos que se muestra aquí puede producirse dentro de un proceso PMP o dentro de un proceso de aplicación.

 

El descodificador recibe datos de vídeo cifrados y comprimidos de un origen externo. También se supone que el descodificador también recibe una clave criptográfica para descifrar estos datos. En este tema no se describe el intercambio de claves entre el origen de vídeo y el descodificador, pero el PMP define un mecanismo posible. La GPU no está implicada en esta fase.

Para la descodificación acelerada por hardware, el descodificador de software pasa contenido de vídeo comprimido a la GPU. Para proteger este contenido, el descodificador vuelve a cifrar los datos, normalmente mediante AES-CTR, antes de pasarlos al acelerador de hardware. Se define un mecanismo de intercambio de claves entre el descodificador y el controlador de gráficos.

Los fotogramas de vídeo descodificados se almacenan en la memoria de vídeo, por lo general de forma clara. En este momento, los fotogramas se procesan y, a continuación, se presentan. Hay dos opciones principales para la presentación.

-   Cuando se usa la API D3D9, los fotogramas se pueden presentar mediante una superposición de hardware. El hardware no se admite en exceso en D3D11. Para obtener más información, vea [Compatibilidad con la superposición de hardware.](hardware-overlay-support.md)
-   La administración de ventanas de escritorio (DWM) puede presentar fotogramas mediante una superficie compartida.

El último paso consiste en mostrar el marco en el monitor, que puede requerir la protección de vínculos entre la tarjeta gráfica y el dispositivo de visualización. Un ejemplo de protección de vínculos es High-Bandwidth Digital Content Protection (HDCP). La protección de vínculos se configura [mediante Output Protection Manager](output-protection-manager.md) (OPM). En este tema no se describe OPM; Para obtener más información, vea [Uso de Output Protection Manager.](using-output-protection-manager.md)

## <a name="overview-of-the-decoding-process"></a>Información general del proceso de descodización

Durante la descodificación acelerada por hardware, el descodificador de software debe pasar datos de vídeo comprimidos a la tarjeta gráfica. En el caso del contenido Premium, estos datos normalmente se deben cifrar, mediante el cifrado de clave simétrica, antes de enviarse a la GPU.

Para cifrar el vídeo para descodificar, el descodificador de software usa las interfaces siguientes:

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Representa el dispositivo descodificador, también denominado acelerador.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Representa una sesión criptográfica, que proporciona la clave de cifrado.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Representa un canal autenticado, que permite al descodificador de software asociar la sesión criptográfica con el descodificador.

![diagrama que muestra las interfaces de decoding de direct3d9.](images/d3d9video02.png)

Todas estas interfaces se obtienen del dispositivo Direct3D11, como se muestra a continuación:



| Interfaz                                                        | Creación                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Llame [**a ID3D11VideoDevice::CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview). El tipo de descodificador se identifica mediante un GUID de perfil. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Llame [**a ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Llame [**a ID3D11VideoDevice::CreateAuthenticatedChannel.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel)                                             |



 

> [!Note]  
> Para obtener un puntero a la [**interfaz ID3D11VideoDevice,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en [**la interfaz ID3D11Device.**](/windows/win32/api/d3d11/nn-d3d11-id3d11device)

 

El canal autenticado proporciona un canal de comunicación de confianza entre el descodificador de software y el controlador. El canal de comunicación funciona de la siguiente manera:

-   El controlador proporciona una cadena de certificados X.509 cuyo certificado raíz está firmado por Microsoft.
-   El certificado contiene una clave pública RSA para el controlador.
-   El descodificador de software usa la clave pública para enviar al controlador una clave de sesión AES de 128 bits.
-   El descodificador de software envía consultas y comandos al canal autenticado.
-   La clave de sesión se usa para calcular los códigos de autenticación de mensajes (MAC) para las consultas y comandos. El controlador usa los MAC para comprobar la integridad de los datos de consulta o comando, y el descodificador de software los usa para comprobar la integridad de los datos de respuesta del controlador.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Cifrado de búferes de vídeo comprimidos para el descodificador

Esta es una introducción general del proceso de cifrado y decodización:

1.  El descodificador de software recibe un flujo de datos cifrados del origen del vídeo. El descodificador descifra esta secuencia.
2.  El descodificador de software negocia una clave de sesión con la sesión criptográfica.
3.  El descodificador de software usa el canal autenticado para asociar la sesión criptográfica al dispositivo descodificador.
4.  El descodificador de software coloca los datos comprimidos en búferes que obtiene del dispositivo descodificador (acelerador). Para el contenido protegido, el codificador de software cifra los datos que se coloca en los búferes, mediante la clave de sesión para el cifrado.
    > [!Note]  
    > Algunos controladores usan una clave de contenido, en lugar de la clave de sesión, para el cifrado. La clave de contenido podría cambiar de un fotograma al siguiente.

     

5.  El descodificador envía los búferes comprimidos cifrados al acelerador. Para AES-CTR, el descodificador también pasa el vector de inicialización. Si se usa una clave de contenido, el descodificador pasa la clave de contenido, cifrada mediante la clave de sesión.

Direct3D11 tiene compatibilidad estándar con AES-CTR de 128 bits, pero está diseñado para extenderse a tipos de cifrado adicionales.

En las cinco secciones siguientes se indican pasos más detallados.

-   [1. Consultar las Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Configurar el canal autenticado](#2-configure-the-authenticated-channel)
-   [3. Configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
-   [4. Asociación del descodificador a la sesión criptográfica](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Consultar las Content Protection del controlador

Antes de intentar aplicar el cifrado, obtenga las funcionalidades de protección de contenido del controlador.

1.  Obtenga un puntero a la interfaz ID3D11Device.
2.  Llame [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la [**interfaz ID3D11VideoDevice.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice)
3.  Llame [**a ID3D11VideoDevice::GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps). Este método rellena una estructura [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) con las funcionalidades de protección de contenido del controlador.

En concreto, busque las siguientes funcionalidades:

-   Si el **miembro Caps** contiene la **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** o **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE,** el controlador puede realizar el cifrado.
-   Si el **miembro Caps** contiene la **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY,** el controlador usa una clave de contenido independiente para el descifrado.
-   Llame [**a ID3D11VideoDevice::CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) para determinar qué tipos de intercambios de claves admite el controlador para generar la clave de sesión.

Las funcionalidades adicionales se indican en el **miembro Caps.**

### <a name="2-configure-the-authenticated-channel"></a>2. Configurar el canal autenticado

El siguiente paso consiste en configurar el canal autenticado.

1.  Llame [**a ID3D11VideoDevice::CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) para crear el canal autenticado. Para el *parámetro ChannelType,* especifique un tipo de canal que coincida con las funciones del controlador.
    -   El **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** de canal correspondiente a **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   El **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** de canal correspondiente a **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    El **método CreateAuthenticatedChannel** devuelve un puntero a la [**interfaz ID3D11AuthenticatedChannel.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel)
2.  Llame [**a ID3D11AuthenticatedChannel::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) para obtener el tamaño del certificado X.509 del controlador. Asigne un búfer del tamaño necesario.
3.  Llame [**a ID3D11AuthenticatedChannel::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) para obtener el certificado. El método copia el certificado en el búfer asignado en el paso anterior.
4.  Compruebe que microsoft firmó el certificado del controlador y que no se ha revocado.
5.  Obtenga la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Esta clave de sesión se usa para firmar los datos que se envían al canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame [**a ID3D11VideoContext::NegotiateAuthenticatedChannelKeyExchange para**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) enviar la clave de sesión cifrada al controlador.
8.  Inicialice el canal seguro de la siguiente manera:
    1.  Rellene una estructura [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) como se describe en la documentación.
    2.  Envíe el [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) mediante una llamada a [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) como se describe en la sección Envío de comandos [de canal autenticados.](#sending-authenticated-channel-commands) Este comando contiene los números de secuencia iniciales de los comandos y las consultas que se envían al canal autenticado.
9.  Compruebe el tipo de canal enviando una [**consulta D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) al canal autenticado, como se describe en la sección Envío de consultas de [canal autenticadas.](#sending-authenticated-channel-queries) Compruebe que el tipo de canal coincide con lo que especificó en el [**método CreateAuthenticatedChannel.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

### <a name="3-configure-the-cryptographic-session"></a>3. Configurar la sesión criptográfica

A continuación, configure la sesión criptográfica y establezca la clave de sesión.

1.  Llame [**a ID3D11VideoDevice::CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para crear la sesión criptográfica. Este método devuelve un puntero a la [**interfaz ID3D11CryptoSession.**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)
2.  Llame [**a ID3D11CryptoSession::GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) para obtener el tamaño del certificado X.509 del controlador. Asigne un búfer del tamaño necesario.
3.  Llame [**a ID3D11CryptoSession::GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) para obtener el certificado. El método copia el certificado en el búfer asignado en el paso anterior.
4.  Compruebe que microsoft firmó el certificado del controlador y que no se ha revocado.
5.  Obtenga la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Se trata de una clave de sesión independiente de la clave de sesión del canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame [**a ID3D11VideoContext::NegotiateCryptoSessionKeyExchange para**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) enviar la clave de sesión cifrada al controlador.
8.  Si las funcionalidades de protección de **contenido incluyen 3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**, cree una clave de contenido RSA aleatoria. Se usará más adelante en el proceso de descodización.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. Asociar el descodificador a la sesión criptográfica

A continuación, asocie el dispositivo descodificador con el dispositivo Direct3D11 y la sesión criptográfica, como se muestra a continuación:

1.  Obtenga un identificador para el dispositivo Direct3D11 mediante el envío de una [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) consulta al canal autenticado.
2.  Rellene una [**estructura D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) con la siguiente información:
    -   Establezca el **miembro DecodeHandle** en el identificador devuelto desde [**ID3D11VideoDecoder::GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle).
    -   Establezca el **miembro CryptoSessionHandle** en el identificador devuelto desde [**ID3D11CryptoSession::GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle).
    -   Establezca el **miembro DeviceHandle** en el identificador de dispositivo Direct3D11.
3.  Llame [**a**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) [**ID3D11VideoContext::ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) para enviar un D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION al canal autenticado.

En el diagrama siguiente se muestra el intercambio de identificadores:

![diagrama que muestra cómo está asociado el descodificador dxva a la sesión criptográfica.](images/d3d9video03.png)

El descodificador de software ahora puede usar la clave de sesión criptográfica para cifrar los búferes de vídeo comprimidos. Cada búfer comprimido tendrá su propio vector de inicialización (IV) especificado en el **miembro pIV** de la [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) estructura.

## <a name="sending-authenticated-channel-commands"></a>Envío de comandos de canal autenticados

Se define un conjunto de comandos para configurar el canal autenticado y establecer varias protecciones de contenido. Para obtener una lista de comandos, [vea Content Protection Comandos](content-protection-commands.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es una [**estructura D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) seguida de campos adicionales. Rellene la estructura **D3D11_AUTHENTICATED_CONFIGURE_INPUT** como se muestra en la tabla siguiente.

    
| Miembro | Descripción | 
|--------|-------------|
| <strong>Omac</strong> | Omita este campo por ahora. | 
| <strong>ConfigureType</strong> | GUID que identifica el comando. Para obtener una lista de comandos, <a href="content-protection-commands.md">vea Content Protection Comandos</a>. | 
| <strong>hChannel</strong> | Identificador del canal autenticado. | 
| <strong>SequenceNumber</strong> | El número de secuencia global. El primer número de secuencia se especifica mediante el envío de <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> comando. Cada vez que envíe otro comando, incremente este número en 1. El número de secuencia protege contra ataques de reproducción.    <blockquote>    [!Note]<br />    Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.    </blockquote><br /><br /> | 


    

     

2.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del **miembro omac** de la estructura de entrada. A continuación, copie este valor de etiqueta en el **miembro omac.**
3.  Llame [**a ID3D11VideoContext::ConfigureAuthenticatedChannel.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel)
4.  El controlador coloca la salida del comando en la [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) estructura .
5.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del **miembro omac** de la estructura de salida. Compare esto con el valor del **miembro omac.** Se producirá un error si no coinciden.
6.  Compare los valores de los **miembros ConfigureType**, **hChannel** y **SequenceNumber** de la estructura de salida con los valores de esos miembros. Se producirá un error si no coinciden.
7.  Incremente el número de secuencia para el comando siguiente.

## <a name="sending-authenticated-channel-queries"></a>Envío de consultas de canal autenticadas

Se define un conjunto de consultas para recuperar información sobre el canal autenticado. Para obtener una lista de consultas, [vea Content Protection Queries](content-protection-queries.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre [**es**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) D3D11_AUTHENTICATED_QUERY_INPUT estructura, posiblemente seguida de campos adicionales. Rellene la estructura **D3D11_AUTHENTICATED_QUERY_INPUT** como se muestra en la tabla siguiente.

    
| Miembro | Descripción | 
|--------|-------------|
| <strong>Querytype</strong> | GUID que identifica la consulta. Para obtener una lista de consultas, <a href="content-protection-queries.md">vea Content Protection Queries</a>. | 
| <strong>hChannel</strong> | Identificador del canal autenticado. | 
| <strong>SequenceNumber</strong> | El número de secuencia global. El primer número de secuencia se especifica mediante el envío de <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> comando. Cada vez que envíe otra consulta, incremente este número en 1. El número de secuencia protege contra ataques de reproducción.    <blockquote>    [!Note]<br />    Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.    </blockquote><br /><br /> | 


    

     

2.  Llame [**a ID3D11VideoContext::QueryAuthenticatedChannel.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel)
3.  El controlador coloca la salida de la consulta en una [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) estructura. Esta estructura va seguida de campos adicionales, según el tipo de consulta.
4.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del **miembro omac** de la estructura de salida. Compare esto con el valor del **miembro omac.** Se producirá un error si no coinciden.
5.  Compare los valores de los **miembros ConfigureType**, **hChannel** y **SequenceNumber** de la estructura de salida con los valores de esos miembros. Se producirá un error si no coinciden.
6.  Incremente el número de secuencia de la siguiente consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 
