---
description: Describe el contenido de vídeo&\# 8211; capacidades de protección que puede proporcionar un controlador de gráficos.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based Content Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbc1a0f88cae199b9aab38e5ec429ea5427f44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567208"
---
# <a name="gpu-based-content-protection"></a>GPU-Based Content Protection

En este tema se describe el contenido de vídeo: capacidades de protección que puede proporcionar un controlador de gráficos.

-   [Introducción](#introduction)
-   [Información general sobre el proceso de descodificación](#overview-of-the-decoding-process)
-   [Cifrado de búferes de vídeo comprimidos para el descodificador](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. consultar las capacidades Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. configurar el canal autenticado](#2-configure-the-authenticated-channel)
    -   [3. configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
    -   [4. obtener un identificador para el dispositivo descodificador de DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. asociar el descodificador de DXVA a la sesión criptográfica](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Envío de comandos de canal autenticado](#sending-authenticated-channel-commands)
-   [Envío de consultas de canales autenticadas](#sending-authenticated-channel-queries)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En el diagrama siguiente se muestra una vista simplificada de cómo se recorre el contenido de vídeo protegido a través de la canalización.

![diagrama que muestra el contenido de vídeo protegido.](images/d3d9video01.png)

> [!Note]  
> La [ruta de acceso a los medios protegidos](protected-media-path.md) (PMP) no se muestra en este diagrama. El flujo de datos que se muestra aquí puede aparecer dentro de un proceso de PMP o dentro de un proceso de aplicación.

 

El descodificador recibe datos de vídeo cifrados y comprimidos de un origen externo. También se supone que el descodificador recibe también una clave criptográfica para descifrar estos datos. En este tema no se describe el intercambio de claves entre el origen y el descodificador de vídeo, pero el PMP define un posible mecanismo. La GPU no está implicada en esta fase.

Para la descodificación acelerada por hardware, el descodificador de software pasa el contenido de vídeo comprimido a la GPU. Para proteger este contenido, el descodificador vuelve a cifrar los datos, normalmente mediante AES-CTR, antes de pasarlos al Acelerador de hardware. Se define un mecanismo de intercambio de claves entre el descodificador y el controlador de gráficos.

Los fotogramas de vídeo descodificados se almacenan en la memoria de vídeo, por lo general, sin cifrar. En este momento, los fotogramas se procesan y se presentan. Hay dos opciones principales para la presentación.

-   Los fotogramas se pueden presentar mediante una superposición de hardware. Para obtener más información, consulte [compatibilidad con la superposición de hardware](hardware-overlay-support.md).
-   Los fotogramas se pueden presentar mediante la ventana de escritorio administrar (DWM) mediante una superficie compartida.

El último paso es mostrar el fotograma en el monitor, que puede requerir protección de vínculos entre la tarjeta gráfica y el dispositivo de pantalla. Un ejemplo de protección de vínculos es High-Bandwidth Content Protection digital (HDCP). La protección de vínculos se configura mediante el [Administrador de protección de salida](output-protection-manager.md) (OPM). En este tema no se describe OPM; para obtener más información, consulte [uso del administrador de protección de salida](using-output-protection-manager.md).

## <a name="overview-of-the-decoding-process"></a>Información general sobre el proceso de descodificación

Durante la descodificación acelerada por hardware, el descodificador de software debe pasar datos de vídeo comprimidos a la tarjeta gráfica. En el caso de contenido premium, estos datos normalmente se deben cifrar mediante el cifrado de clave simétrica antes de enviarlos a la GPU.

Para cifrar el vídeo para la descodificación, el descodificador de software utiliza las siguientes interfaces:

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Representa el dispositivo descodificador de DXVA, también denominado Acelerador.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Representa una sesión de cifrado, que proporciona la clave de cifrado.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Representa un canal autenticado, que permite al descodificador de software asociar la sesión de cifrado con el descodificador de DXVA.

![diagrama que muestra las interfaces de descodificación de Direct3D9.](images/d3d9video02.png)

Todas estas interfaces se obtienen del dispositivo Direct3D, como se indica a continuación:



| Interfaz                                                                | Creación                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Llame a [**IDirectXVideoDecoderService:: CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). El dispositivo descodificador de DXVA se identifica mediante un GUID de Perfil de DXVA. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Llame a [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Llame a [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Para obtener un puntero a la interfaz [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) , llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un dispositivo D3D9Ex.

 

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
3.  El descodificador de software usa el canal autenticado para asociar la sesión criptográfica con el dispositivo descodificador de DXVA.
4.  El descodificador de software coloca los datos comprimidos en los búferes de DXVA que obtiene del dispositivo de descodificador de DXVA (acelerador). Para el contenido protegido, el codificador de software cifra los datos que se colocan en los búferes de DXVA, utilizando la clave de sesión para el cifrado.
    > [!Note]  
    > Algunos controladores usan una clave de contenido, en lugar de la clave de sesión, para el cifrado. La clave de contenido podría cambiar de un marco a otro.

     

5.  El descodificador envía los búferes comprimidos cifrados al acelerador. En el caso de AES-CTR, el descodificador también pasa el vector de inicialización. Si se usa una clave de contenido, el descodificador pasa la clave de contenido, cifrada mediante la clave de sesión.

Direct3D tiene compatibilidad estándar con AES-CTR de 128 bits, pero está diseñado para extenderse a tipos de cifrado adicionales.

Las cinco secciones siguientes proporcionan pasos más detallados.

-   [1. consultar las capacidades Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. configurar el canal autenticado](#2-configure-the-authenticated-channel)
-   [3. configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
-   [4. obtener un identificador para el dispositivo descodificador de DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. asociar el descodificador de DXVA a la sesión criptográfica](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. consultar las capacidades Content Protection del controlador

Antes de intentar aplicar el cifrado, obtenga las capacidades de protección de contenido del controlador.

1.  Obtiene un puntero al dispositivo de Direct3D 9.
2.  Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la interfaz [**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) .
3.  Llame a [**IDirect3DDevice9Video:: GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Este método rellena una estructura [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) con las funcionalidades de protección de contenido del controlador.

En concreto, busque las siguientes funcionalidades:

-   Si el miembro **caps** contiene la marca **D3DCPCAPS_SOFTWARE** o **D3DCPCAPS_HARDWARE** , el controlador puede realizar el cifrado.
-   El miembro **KeyExchangeType** especifica cómo realizar el intercambio de claves para la clave de sesión.
-   Si el miembro **caps** contiene la marca **D3DCPCAPS_CONTENTKEY** , el controlador utiliza una clave de contenido independiente para el cifrado. Esto es importante cuando se genera la clave de sesión.

Las funcionalidades adicionales se indican en el miembro **Cap** .

### <a name="2-configure-the-authenticated-channel"></a>2. configurar el canal autenticado

El siguiente paso consiste en configurar el canal autenticado.

1.  Llame a [**IDirect3DDevice9Video:: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) para crear el canal autenticado. Para el parámetro *ChannelType* , especifique un tipo de canal que coincida con las capacidades del controlador.
    -   El tipo de canal **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** corresponde a **D3DCPCAPS_SOFTWARE**.
    -   El tipo de canal **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** corresponde a **D3DCPCAPS_HARDWARE**.

    El método **CreateAuthenticatedChannel** devuelve un puntero a la interfaz [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) junto con un identificador para el canal. El identificador se usa más adelante para asociar la sesión de cifrado con el canal autenticado.
2.  Llame a [**IDirect3DAuthenticatedChannel9:: GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) para obtener el tamaño del certificado X. 509 del controlador. Asigne un búfer del tamaño requerido.
3.  Llame a [**IDirect3DAuthenticatedChannel9:: GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) para obtener el certificado. El método copia el certificado en el búfer que se asignó en el paso anterior.
4.  Compruebe que el certificado del controlador está firmado por Microsoft y que no se ha revocado.
5.  Obtiene la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Esta clave de sesión se usa para firmar los datos que se envían al canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame a [**IDirect3DAuthenticatedChannel9:: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) para enviar la clave de sesión cifrada al controlador.
8.  Inicialice el canal seguro como se indica a continuación:
    1.  Rellene una estructura de [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) como se describe en la documentación de.
    2.  Envíe el comando [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) llamando a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) como se describe en la sección [envío de comandos de canal autenticado](#sending-authenticated-channel-commands). Este comando contiene los números de secuencia inicial para los comandos y las consultas que se envían al canal autenticado.
9.  Compruebe el tipo de canal mediante el envío de una [**D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) consulta al canal autenticado, como se describe en la sección [envío de consultas de canal autenticado](#sending-authenticated-channel-queries). Compruebe que el tipo de canal coincide con lo que especificó en el método [**CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) .

### <a name="3-configure-the-cryptographic-session"></a>3. configurar la sesión criptográfica

A continuación, configure la sesión criptográfica y establezca la clave de sesión.

1.  Llame a [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) para crear la sesión criptográfica. Este método devuelve un puntero a la interfaz [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) y junto con un identificador a la sesión criptográfica.
2.  Llame a [**IDirect3DCryptoSession9:: GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) para obtener el tamaño del certificado X. 509 del controlador. Asigne un búfer del tamaño requerido.
3.  Llame a [**IDirect3DCryptoSession9:: GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) para obtener el certificado. El método copia el certificado en el búfer que se asignó en el paso anterior.
4.  Compruebe que el certificado del controlador está firmado por Microsoft y que no se ha revocado.
5.  Obtiene la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Se trata de una clave de sesión independiente de la clave de sesión del canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame a [**IDirect3DCryptoSession9:: NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) para enviar la clave de sesión cifrada al controlador.
8.  Si las capacidades de protección de contenido incluyen **D3DCPCAPS_CONTENTKEY**, cree una clave de contenido RSA aleatoria. Se usará más adelante en el proceso de descodificación.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. obtener un identificador para el dispositivo descodificador de DXVA

En el siguiente paso, necesitará un identificador para el dispositivo descodificador de DXVA. Para obtener este identificador, rellene una estructura de DXVA2_DecodeExecuteParams como se indica a continuación:


```C++
HANDLE hDecodeDeviceHandle;

DXVA2_DecodeExecuteParams execParams = {0};
DXVA2_DecodeExtensionData ExtensionExecute = {0};
    
execParams.NumCompBuffers = 0;
execParams.pCompressedBuffers = NULL;
execParams.pExtensionData = &ExtensionExecute;

ExtensionExecute.Function = DXVA2_DECODE_GET_DRIVER_HANDLE;
ExtensionExecute.pPrivateInputData = NULL;
ExtensionExecute.PrivateInputDataSize = 0;
ExtensionExecute.pPrivateOutputData = &hDecodeDeviceHandle;
ExtensionExecute.PrivateOutputDataSize = sizeof(HANDLE);
```



Establezca el miembro **pExtensionData** de la estructura [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) en la dirección de una estructura de [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) .

En la estructura [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) , establezca el miembro de **función** en **DXVA2_DECODE_GET_DRIVER_HANDLE**. Establezca **pPrivateOutputData** en la dirección de un búfer que sea lo suficientemente grande como para almacenar un valor de **identificador** . (En el ejemplo anterior, este búfer es la variable *hDecodeDeviceHandle* ).

A continuación, llame a [**IDirectXVideoDecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) y pase la dirección de la estructura [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) . El identificador del descodificador de DXVA se devuelve en **pPrivateOutputData**.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. asociar el descodificador de DXVA a la sesión criptográfica

A continuación, asocie el dispositivo descodificador de DXVA con el dispositivo Direct3D y la sesión de cifrado, como se indica a continuación:

1.  Obtiene un identificador para el dispositivo descodificador de DXVA, tal como se describe en la sección anterior.
2.  Obtener un identificador para el dispositivo Direct3D mediante el envío de una [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) consulta al canal autenticado.
3.  Rellene una estructura de [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) con la siguiente información:
    -   Establezca el miembro **DXVA2DecodeHandle** en el identificador del dispositivo de descodificador de DXVA.
    -   Establezca el miembro **CryptoSessionHandle** en el identificador de la sesión criptográfica. Este identificador es devuelto por el método [**IDirect3DDevice9Video:: CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) .
    -   Establezca el miembro **DeviceHandle** en el identificador del dispositivo Direct3D.
4.  Llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) para enviar un comando [**D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) al canal autenticado.

En el diagrama siguiente se muestra el intercambio de identificadores:

![diagrama que muestra cómo el descodificador de DXVA está asociado a la sesión criptográfica.](images/d3d9video03.png)

Ahora, el descodificador de software puede usar la clave de sesión criptográfica para cifrar los búferes de vídeo comprimidos. Cada búfer comprimido tendrá su propio vector de inicialización (IV) especificado en el miembro **pvPVPState** de la estructura [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) .

## <a name="sending-authenticated-channel-commands"></a>Envío de comandos de canal autenticado

Se define un conjunto de comandos para configurar el canal autenticado y establecer varias protecciones de contenido. Para obtener una lista de comandos, vea [comandos Content Protection](content-protection-commands.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es una estructura de [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) seguido de campos adicionales. Rellene la estructura **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** como se muestra en la tabla siguiente.

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
    <td>El número de secuencia global. El primer número de secuencia se especifica mediante el envío de un comando <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Cada vez que envíe otro comando, incremente este número en 1. El número de secuencia se protege contra los ataques de reproducción.
    <blockquote>
    [!Note]<br />
Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **OMAC** de la estructura de entrada. A continuación, copie este valor de etiqueta en el miembro **OMAC** .
3.  Llame a [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  El controlador coloca el resultado del comando en la estructura [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) .
5.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **OMAC** de la estructura de salida. Compárelo con el valor del miembro **OMAC** . Se produce un error si no coinciden.
6.  Compare los valores de los miembros **ConfigureType**, **hChannel** y **SequenceNumber** en la estructura de salida con los valores de esos miembros. Se produce un error si no coinciden.
7.  Incremente el número de secuencia para el siguiente comando.

## <a name="sending-authenticated-channel-queries"></a>Envío de consultas de canales autenticadas

Se define un conjunto de consultas para recuperar información sobre el canal autenticado. Para obtener una lista de consultas, vea [consultas de Content Protection](content-protection-queries.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es una estructura de [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) , posiblemente seguida de campos adicionales. Rellene la estructura **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** como se muestra en la tabla siguiente.

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
    <td>El número de secuencia global. El primer número de secuencia se especifica mediante el envío de un comando <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> . Cada vez que envíe otra consulta, incremente este número en 1. El número de secuencia se protege contra los ataques de reproducción.
    <blockquote>
    [!Note]<br />
Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.
    </blockquote>
    <br/> <br/></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Llame a [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  El controlador coloca el resultado de la consulta en una estructura de [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) . Esta estructura va seguida de campos adicionales, en función del tipo de consulta.
4.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del miembro **OMAC** de la estructura de salida. Compárelo con el valor del miembro **OMAC** . Se produce un error si no coinciden.
5.  Compare los valores de los miembros **ConfigureType**, **hChannel** y **SequenceNumber** en la estructura de salida con los valores de esos miembros. Se produce un error si no coinciden.
6.  Incremente el número de secuencia de la siguiente consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
