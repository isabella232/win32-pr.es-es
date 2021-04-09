---
description: En este tema se describe el contenido de vídeo&\# 8211; capacidades de protección que puede proporcionar un controlador de gráficos.
ms.assetid: 3FDB4908-C75D-4AE0-B32E-93F840E4F30A
title: GPU-Based Content Protection con vídeo de D3D11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78097492d375d50688f2472f5d2de99cc21f8594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080310"
---
# <a name="gpu-based-content-protection-with-d3d11-video"></a>GPU-Based Content Protection con vídeo de D3D11

En este tema se describe el contenido de vídeo: capacidades de protección que puede proporcionar un controlador de gráficos.

-   [Introducción](#introduction)
-   [Información general sobre el proceso de descodificación](#overview-of-the-decoding-process)
-   [Cifrado de búferes de vídeo comprimidos para el descodificador](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. consultar las capacidades Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurar el canal autenticado](#2-configure-the-authenticated-channel)
    -   [3. configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
    -   [4. asociar el descodificador a la sesión criptográfica](#4-associate-the-decoder-with-the-cryptographic-session)
-   [Envío de comandos de canal autenticado](#sending-authenticated-channel-commands)
-   [Envío de consultas de canales autenticadas](#sending-authenticated-channel-queries)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En el diagrama siguiente se muestra una vista simplificada de cómo se recorre el contenido de vídeo protegido a través de la canalización.

![diagrama que muestra el contenido de vídeo protegido.](images/d3d9video01.png)

> [!Note]
>
> La [ruta de acceso a los medios protegidos](protected-media-path.md) (PMP) no se muestra en este diagrama. El flujo de datos que se muestra aquí puede aparecer dentro de un proceso de PMP o dentro de un proceso de aplicación.

 

El descodificador recibe datos de vídeo cifrados y comprimidos de un origen externo. También se supone que el descodificador recibe también una clave criptográfica para descifrar estos datos. En este tema no se describe el intercambio de claves entre el origen y el descodificador de vídeo, pero el PMP define un posible mecanismo. La GPU no está implicada en esta fase.

Para la descodificación acelerada por hardware, el descodificador de software pasa el contenido de vídeo comprimido a la GPU. Para proteger este contenido, el descodificador vuelve a cifrar los datos, normalmente mediante AES-CTR, antes de pasarlos al Acelerador de hardware. Se define un mecanismo de intercambio de claves entre el descodificador y el controlador de gráficos.

Los fotogramas de vídeo descodificados se almacenan en la memoria de vídeo, por lo general, sin cifrar. En este momento, los fotogramas se procesan y se presentan. Hay dos opciones principales para la presentación.

-   Cuando se usa la API de D3D9, se pueden presentar fotogramas mediante una superposición de hardware. El hardware no es compatible con D3D11. Para obtener más información, consulte [compatibilidad con la superposición de hardware](hardware-overlay-support.md).
-   Los fotogramas se pueden presentar mediante la ventana de escritorio administrar (DWM) mediante una superficie compartida.

El último paso es mostrar el fotograma en el monitor, que puede requerir protección de vínculos entre la tarjeta gráfica y el dispositivo de pantalla. Un ejemplo de protección de vínculos es High-Bandwidth Content Protection digital (HDCP). La protección de vínculos se configura mediante el [Administrador de protección de salida](output-protection-manager.md) (OPM). En este tema no se describe OPM; para obtener más información, consulte [uso del administrador de protección de salida](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Información general sobre el proceso de descodificación

Durante la descodificación acelerada por hardware, el descodificador de software debe pasar datos de vídeo comprimidos a la tarjeta gráfica. En el caso de contenido premium, estos datos normalmente se deben cifrar mediante el cifrado de clave simétrica antes de enviarlos a la GPU.

Para cifrar el vídeo para la descodificación, el descodificador de software utiliza las siguientes interfaces:

-   [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder). Representa el dispositivo descodificador, también denominado Acelerador.
-   [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession). Representa una sesión de cifrado, que proporciona la clave de cifrado.
-   [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel). Representa un canal autenticado, que permite al descodificador de software asociar la sesión de cifrado con el descodificador.

![diagrama que muestra las interfaces de descodificación de Direct3D9.](images/d3d9video02.png)

Todas estas interfaces se obtienen del dispositivo Direct3D 11, como se indica a continuación:



| Interfaz                                                        | Creación                                                                                                                                                |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11VideoDecoder**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder)                 | Llame a [**ID3D11VideoDevice:: CreateVideoDecoder**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview). El tipo de descodificador se identifica mediante un GUID de perfil. |
| [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession)               | Llame a [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession).                                                           |
| [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) | Llame a [**ID3D11VideoDevice:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel).                                             |



 

> [!Note]  
> Para obtener un puntero a la interfaz [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) , llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) .

 

El canal autenticado proporciona un canal de comunicación de confianza entre el descodificador de software y el controlador. El canal de comunicación funciona de la siguiente manera:

-   El controlador proporciona una cadena de certificados X. 509 cuyo certificado raíz está firmado por Microsoft.
-   El certificado contiene una clave pública RSA para el controlador.
-   El descodificador de software usa la clave pública para enviar al controlador una clave de sesión AES de 128 bits.
-   El descodificador de software envía consultas y comandos al canal autenticado.
-   La clave de sesión se usa para calcular códigos de autenticación de mensajes (Mac) para las consultas y los comandos. El controlador utiliza los equipos Mac para comprobar la integridad de los datos de consulta y comando, y el descodificador de software los usa para comprobar la integridad de los datos de respuesta del controlador.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Cifrado de búferes de vídeo comprimidos para el descodificador

A continuación se muestra una introducción de alto nivel del proceso de cifrado y descodificación:

1.  El descodificador de software recibe un flujo de datos cifrados del origen de vídeo. El descodificador descifra esta secuencia.
2.  El descodificador de software negocia una clave de sesión con la sesión criptográfica.
3.  El descodificador de software usa el canal autenticado para asociar la sesión de cifrado con el dispositivo descodificador.
4.  El descodificador de software coloca los datos comprimidos en los búferes que obtiene del dispositivo descodificador (acelerador). Para el contenido protegido, el codificador de software cifra los datos que se colocan en los búferes con la clave de sesión para el cifrado.
    > [!Note]  
    > Algunos controladores usan una clave de contenido, en lugar de la clave de sesión, para el cifrado. La clave de contenido podría cambiar de un marco a otro.

     

5.  El descodificador envía los búferes comprimidos cifrados al acelerador. En el caso de AES-CTR, el descodificador también pasa el vector de inicialización. Si se usa una clave de contenido, el descodificador pasa la clave de contenido, cifrada mediante la clave de sesión.

Direct3D 11 tiene compatibilidad estándar con AES-CTR de 128 bits, pero está diseñado para extenderse a tipos de cifrado adicionales.

Las cinco secciones siguientes proporcionan pasos más detallados.

-   [1. consultar las capacidades Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurar el canal autenticado](#2-configure-the-authenticated-channel)
-   [3. configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
-   [4. asociar el descodificador a la sesión criptográfica](#4-associate-the-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. consultar las capacidades Content Protection del controlador

Antes de intentar aplicar el cifrado, obtenga las capacidades de protección de contenido del controlador.

1.  Obtiene un puntero a la interfaz ID3D11Device.
2.  Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz [**ID3D11VideoDevice**](/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice) .
3.  Llame a [**ID3D11VideoDevice:: GetContentProtectionCaps**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-getcontentprotectioncaps). Este método rellena una estructura de [**D3D11_VIDEO_CONTENT_PROTECTION_CAPS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_content_protection_caps) con las funcionalidades de protección de contenido del controlador.

En concreto, busque las siguientes funcionalidades:

-   Si el miembro **caps** contiene la marca **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE** o **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE** , el controlador puede realizar el cifrado.
-   Si el miembro **caps** contiene la marca **D3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY** , el controlador utiliza una clave de contenido independiente para el descifrado.
-   Llame a [**ID3D11VideoDevice:: CheckCryptoKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-checkcryptokeyexchange) para determinar qué tipos de intercambios de clave admite el controlador para generar la clave de sesión.

Las funcionalidades adicionales se indican en el miembro **Cap** .

### <a name="2-configure-the-authenticated-channel"></a>2. configurar el canal autenticado

El siguiente paso consiste en configurar el canal autenticado.

1.  Llame a [**ID3D11VideoDevice:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createauthenticatedchannel) para crear el canal autenticado. Para el parámetro *ChannelType* , especifique un tipo de canal que coincida con las capacidades del controlador.
    -   El tipo de canal **D3D11_AUTHENTICATED_CHANNEL_DRIVER_SOFTWARE** corresponde a **D3D11_CONTENT_PROTECTION_CAPS_SOFTWARE**.
    -   El tipo de canal **D3D11_AUTHENTICATED_CHANNEL_DRIVER_HARDWARE** corresponde a **D3D11_CONTENT_PROTECTION_CAPS_HARDWARE**.

    El método **CreateAuthenticatedChannel** devuelve un puntero a la interfaz [**ID3D11AuthenticatedChannel**](/windows/desktop/api/d3d11/nn-d3d11-id3d11authenticatedchannel) .
2.  Llame a [**ID3D11AuthenticatedChannel:: GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificatesize) para obtener el tamaño del certificado X. 509 del controlador. Asigne un búfer del tamaño requerido.
3.  Llame a [**ID3D11AuthenticatedChannel:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getcertificate) para obtener el certificado. El método copia el certificado en el búfer que se asignó en el paso anterior.
4.  Compruebe que el certificado del controlador está firmado por Microsoft y que no se ha revocado.
5.  Obtiene la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Esta clave de sesión se usa para firmar los datos que se envían al canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame a [**ID3D11VideoContext:: NegotiateAuthenticatedChannelKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiateauthenticatedchannelkeyexchange) para enviar la clave de sesión cifrada al controlador.
8.  Inicialice el canal seguro como se indica a continuación:
    1.  Rellene una estructura de [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) como se describe en la documentación de.
    2.  Envíe el comando [**D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input) llamando a [**ID3D11VideoContext:: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) tal y como se describe en la sección [envío de comandos de canal autenticado](#sending-authenticated-channel-commands). Este comando contiene los números de secuencia inicial para los comandos y las consultas que se envían al canal autenticado.
9.  Compruebe el tipo de canal mediante el envío de una [**D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output) consulta al canal autenticado, como se describe en la sección [envío de consultas de canal autenticado](#sending-authenticated-channel-queries). Compruebe que el tipo de canal coincide con lo que especificó en el método [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurar la sesión criptográfica

A continuación, configure la sesión criptográfica y establezca la clave de sesión.

1.  Llame a [**ID3D11VideoDevice:: CreateCryptoSession**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createcryptosession) para crear la sesión criptográfica. Este método devuelve un puntero a la interfaz [**ID3D11CryptoSession**](/windows/desktop/api/d3d11/nn-d3d11-id3d11cryptosession) .
2.  Llame a [**ID3D11CryptoSession:: GetCertificateSize**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificatesize) para obtener el tamaño del certificado X. 509 del controlador. Asigne un búfer del tamaño requerido.
3.  Llame a [**ID3D11CryptoSession:: GetCertificate**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcertificate) para obtener el certificado. El método copia el certificado en el búfer que se asignó en el paso anterior.
4.  Compruebe que el certificado del controlador está firmado por Microsoft y que no se ha revocado.
5.  Obtiene la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Se trata de una clave de sesión independiente de la clave de sesión del canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame a [**ID3D11VideoContext:: NegotiateCryptoSessionKeyExchange**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-negotiatecryptosessionkeyexchange) para enviar la clave de sesión cifrada al controlador.
8.  Si las capacidades de protección de contenido incluyen **3D11_CONTENT_PROTECTION_CAPS_CONTENT_KEY**, cree una clave de contenido RSA aleatoria. Se usará más adelante en el proceso de descodificación.

### <a name="4-associate-the-decoder-with-the-cryptographic-session"></a>4. asociar el descodificador a la sesión criptográfica

A continuación, asocie el dispositivo descodificador con el dispositivo Direct3D 11 y la sesión de cifrado, como se indica a continuación:

1.  Obtener un identificador para el dispositivo Direct3D 11 mediante el envío de una consulta [**D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output) al canal autenticado.
2.  Rellene una estructura de [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) con la siguiente información:
    -   Establezca el miembro **DecodeHandle** en el identificador devuelto de [**ID3D11VideoDecoder:: GetDriverHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle).
    -   Establezca el miembro **CryptoSessionHandle** en el identificador devuelto de [**ID3D11CryptoSession:: GetCryptoSessionHandle**](/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle).
    -   Establezca el miembro **DeviceHandle** en el identificador de dispositivo Direct3D 11.
3.  Llame a [**ID3D11VideoContext:: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel) para enviar un comando [**D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input) al canal autenticado.

En el diagrama siguiente se muestra el intercambio de identificadores:

![diagrama que muestra cómo el descodificador de DXVA está asociado a la sesión criptográfica.](images/d3d9video03.png)

Ahora, el descodificador de software puede usar la clave de sesión criptográfica para cifrar los búferes de vídeo comprimidos. Cada búfer comprimido tendrá su propio vector de inicialización (IV) especificado en el miembro **PIV** de la estructura [**D3D11_VIDEO_DECODER_BUFFER_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_buffer_desc) .

## <a name="sending-authenticated-channel-commands"></a>Envío de comandos de canal autenticado

Se define un conjunto de comandos para configurar el canal autenticado y establecer varias protecciones de contenido. Para obtener una lista de comandos, vea [comandos Content Protection](content-protection-commands.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es una estructura de [**D3D11_AUTHENTICATED_CONFIGURE_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input) seguido de campos adicionales. Rellene la estructura **D3D11_AUTHENTICATED_CONFIGURE_INPUT** como se muestra en la tabla siguiente.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Miembro</th>
    <th>Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>omac</strong></td>
    <td>Omitir este campo por ahora.</td>
    </tr>
    <tr class="even">
    <td><strong>ConfigureType</strong></td>
    <td>GUID que identifica el comando. Para obtener una lista de comandos, vea <a href="content-protection-commands.md">comandos Content Protection</a>.</td>
    </tr>
    <tr class="odd">
    <td><strong>hChannel</strong></td>
    <td>Identificador del canal autenticado.</td>
    </tr>
    <tr class="even">
    <td><strong>SequenceNumber</strong></td>
    <td>El número de secuencia global. El primer número de secuencia se especifica mediante el envío de un comando <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> . Cada vez que envíe otro comando, incremente este número en 1. El número de secuencia se protege contra los ataques de reproducción.
    <blockquote>
    [!Note]<br />
Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **OMAC** de la estructura de entrada. A continuación, copie este valor de etiqueta en el miembro **OMAC** .
3.  Llame a [**ID3D11VideoContext:: ConfigureAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel).
4.  El controlador coloca el resultado del comando en la estructura [**D3D11_AUTHENTICATED_CONFIGURE_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_output) .
5.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **OMAC** de la estructura de salida. Compárelo con el valor del miembro **OMAC** . Se produce un error si no coinciden.
6.  Compare los valores de los miembros **ConfigureType**, **hChannel** y **SequenceNumber** en la estructura de salida con los valores de esos miembros. Se produce un error si no coinciden.
7.  Incremente el número de secuencia para el siguiente comando.

## <a name="sending-authenticated-channel-queries"></a>Envío de consultas de canales autenticadas

Se define un conjunto de consultas para recuperar información sobre el canal autenticado. Para obtener una lista de consultas, vea [consultas de Content Protection](content-protection-queries.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es una estructura de [**D3D11_AUTHENTICATED_QUERY_INPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_input) , posiblemente seguida de campos adicionales. Rellene la estructura **D3D11_AUTHENTICATED_QUERY_INPUT** como se muestra en la tabla siguiente.

    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Miembro</th>
    <th>Descripción</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><strong>QueryType</strong></td>
    <td>GUID que identifica la consulta. Para obtener una lista de consultas, vea <a href="content-protection-queries.md">consultas de Content Protection</a>.</td>
    </tr>
    <tr class="even">
    <td><strong>hChannel</strong></td>
    <td>Identificador del canal autenticado.</td>
    </tr>
    <tr class="odd">
    <td><strong>SequenceNumber</strong></td>
    <td>El número de secuencia global. El primer número de secuencia se especifica mediante el envío de un comando <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input"><strong>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</strong></a> . Cada vez que envíe otra consulta, incremente este número en 1. El número de secuencia se protege contra los ataques de reproducción.
    <blockquote>
    [!Note]<br />
Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Llame a [**ID3D11VideoContext:: QueryAuthenticatedChannel**](/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel).
3.  El controlador coloca el resultado de la consulta en una estructura de [**D3D11_AUTHENTICATED_QUERY_OUTPUT**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output) . Esta estructura va seguida de campos adicionales, en función del tipo de consulta.
4.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **OMAC** de la estructura de salida. Compárelo con el valor del miembro **OMAC** . Se produce un error si no coinciden.
5.  Compare los valores de los miembros **ConfigureType**, **hChannel** y **SequenceNumber** en la estructura de salida con los valores de esos miembros. Se produce un error si no coinciden.
6.  Incremente el número de secuencia de la siguiente consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 11](direct3d-11-video-apis.md)
</dt> </dl>

 

 
