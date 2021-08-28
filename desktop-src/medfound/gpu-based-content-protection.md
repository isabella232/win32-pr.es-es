---
description: Describe el contenido de vídeo&\# 8211;funcionalidades de protección que un controlador de gráficos puede proporcionar.
ms.assetid: FD0625BB-484A-43E6-8931-DB635D4F017F
title: GPU-Based Content Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e09829984273c35524fe9c8f3cd19e759e18dbc
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465042"
---
# <a name="gpu-based-content-protection"></a>GPU-Based Content Protection

En este tema se describen las funcionalidades de protección del contenido de vídeo que puede proporcionar un controlador de gráficos.

-   [Introducción](#introduction)
-   [Información general sobre el proceso de descodización](#overview-of-the-decoding-process)
-   [Cifrado de búferes de vídeo comprimidos para el descodificador](#encrypting-compressed-video-buffers-for-the-decoder)
    -   [1. Consultar las Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
    -   [2. Configuración del canal autenticado](#2-configure-the-authenticated-channel)
    -   [3. Configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
    -   [4. Obtener un identificador para el dispositivo descodificador DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
    -   [5. Asociar el descodificador DXVA con la sesión criptográfica](#5-associate-the-dxva-decoder-with-the-cryptographic-session)
-   [Envío de comandos de canal autenticados](#sending-authenticated-channel-commands)
-   [Envío de consultas de canal autenticadas](#sending-authenticated-channel-queries)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

En el diagrama siguiente se muestra una vista simplificada de cómo viaja el contenido de vídeo protegido a través de la canalización que se va a representar.

![diagrama que muestra el contenido de vídeo protegido.](images/d3d9video01.png)

> [!Note]  
> La [ruta de acceso multimedia](protected-media-path.md) protegida (PMP) no se muestra en este diagrama. El flujo de datos que se muestra aquí puede producirse dentro de un proceso PMP o dentro de un proceso de aplicación.

 

El descodificador recibe datos de vídeo cifrados y comprimidos de un origen externo. También se supone que el descodificador también recibe una clave criptográfica para descifrar estos datos. En este tema no se describe el intercambio de claves entre el origen de vídeo y el descodificador, pero el PMP define un mecanismo posible. La GPU no está implicada en esta fase.

Para la descodificación acelerada por hardware, el descodificador de software pasa contenido de vídeo comprimido a la GPU. Para proteger este contenido, el descodificador vuelve a cifrar los datos, normalmente mediante AES-CTR, antes de pasarlos al acelerador de hardware. Se define un mecanismo de intercambio de claves entre el descodificador y el controlador de gráficos.

Los fotogramas de vídeo descodificados se almacenan en la memoria de vídeo, por lo general de forma clara. En este momento, los fotogramas se procesan y, a continuación, se presentan. Hay dos opciones principales para la presentación.

-   Los fotogramas se pueden presentar mediante una superposición de hardware. Para obtener más información, vea [Compatibilidad con la superposición de hardware.](hardware-overlay-support.md)
-   La administración de ventanas de escritorio (DWM) puede presentar fotogramas mediante una superficie compartida.

El último paso consiste en mostrar el marco en el monitor, lo que puede requerir protección de vínculos entre la tarjeta gráfica y el dispositivo de visualización. Un ejemplo de protección de vínculos es High-Bandwidth Digital Content Protection (HDCP). La protección de vínculos se configura [mediante Output Protection Manager](output-protection-manager.md) (OPM). En este tema no se describe OPM; Para obtener más información, vea [Uso de Output Protection Manager.](using-output-protection-manager.md)

## <a name="overview-of-the-decoding-process"></a>Información general sobre el proceso de descodización

Durante la descodificación acelerada por hardware, el descodificador de software debe pasar datos de vídeo comprimidos a la tarjeta gráfica. En el caso del contenido Premium, estos datos normalmente deben cifrarse, mediante el cifrado de clave simétrica, antes de enviarse a la GPU.

Para cifrar el vídeo para la descodificación, el descodificador de software usa las interfaces siguientes:

-   [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder). Representa el dispositivo descodificador DXVA, también denominado acelerador.
-   [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9). Representa una sesión criptográfica, que proporciona la clave de cifrado.
-   [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9). Representa un canal autenticado, que permite al descodificador de software asociar la sesión criptográfica con el descodificador DXVA.

![diagrama que muestra las interfaces de decoding de direct3d9.](images/d3d9video02.png)

Todas estas interfaces se obtienen del dispositivo Direct3D, como se muestra a continuación:



| Interfaz                                                                | Creación                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder)                     | Llame [**a IDirectXVideoDecoderService::CreateVideoDecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder). El dispositivo descodificador DXVA se identifica mediante un GUID de perfil DXVA. |
| [**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)               | Llame [**a IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession).                                                                         |
| [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) | Llame [**a IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).                                                           |



 

> [!Note]  
> Para obtener un puntero a la [**interfaz IDirect3DDevice9Video,**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video) llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un dispositivo D3D9Ex.

 

El canal autenticado proporciona un canal de comunicación de confianza entre el descodificador de software y el controlador. El canal de comunicación funciona de la siguiente manera:

-   El controlador proporciona una cadena de certificados X.509 cuyo certificado raíz está firmado por Microsoft.
-   El certificado contiene una clave pública RSA para el controlador.
-   El descodificador de software usa la clave pública para enviar al controlador una clave de sesión AES de 128 bits.
-   El descodificador de software envía consultas y comandos al canal autenticado.
-   La clave de sesión se usa para calcular los códigos de autenticación de mensajes (MAC) para las consultas y los comandos. El controlador usa los MAC para comprobar la integridad de los datos de consulta o comando, y el descodificador de software los usa para comprobar la integridad de los datos de respuesta del controlador.

## <a name="encrypting-compressed-video-buffers-for-the-decoder"></a>Cifrado de búferes de vídeo comprimidos para el descodificador

Esta es una introducción de alto nivel del proceso de cifrado y decodización:

1.  El descodificador de software recibe una secuencia de datos cifrados del origen de vídeo. El descodificador descifra esta secuencia.
2.  El descodificador de software negocia una clave de sesión con la sesión criptográfica.
3.  El descodificador de software usa el canal autenticado para asociar la sesión criptográfica con el dispositivo descodificador DXVA.
4.  El descodificador de software coloca los datos comprimidos en búferes DXVA que obtiene del dispositivo descodificador DXVA (acelerador). En el caso del contenido protegido, el codificador de software cifra los datos que se coloca en los búferes DXVA mediante la clave de sesión para el cifrado.
    > [!Note]  
    > Algunos controladores usan una clave de contenido, en lugar de la clave de sesión, para el cifrado. La clave de contenido podría cambiar de un fotograma al siguiente.

     

5.  El descodificador envía los búferes comprimidos cifrados al acelerador. Para AES-CTR, el descodificador también pasa el vector de inicialización. Si se usa una clave de contenido, el descodificador pasa la clave de contenido, cifrada mediante la clave de sesión.

Direct3D tiene compatibilidad estándar con AES-CTR de 128 bits, pero está diseñado para extenderse a tipos de cifrado adicionales.

En las cinco secciones siguientes se indican pasos más detallados.

-   [1. Consultar las Content Protection del controlador](#1-query-the-content-protection-capabilities-of-the-driver)
-   [2. Configuración del canal autenticado](#2-configure-the-authenticated-channel)
-   [3. Configurar la sesión criptográfica](#3-configure-the-cryptographic-session)
-   [4. Obtener un identificador para el dispositivo descodificador DXVA](#4-get-a-handle-to-the-dxva-decoder-device)
-   [5. Asociar el descodificador DXVA con la sesión criptográfica](#5-associate-the-dxva-decoder-with-the-cryptographic-session)

### <a name="1-query-the-content-protection-capabilities-of-the-driver"></a>1. Consultar las Content Protection del controlador

Antes de intentar aplicar el cifrado, obtenga las funcionalidades de protección de contenido del controlador.

1.  Obtenga un puntero al dispositivo Direct3D 9.
2.  Llame [**a QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para la [**interfaz IDirect3DDevice9Video.**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)
3.  Llame [**a IDirect3DDevice9Video::GetContentProtectionCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-getcontentprotectioncaps). Este método rellena una estructura [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps) con las funcionalidades de protección de contenido del controlador.

En concreto, busque las siguientes funcionalidades:

-   Si el **miembro Caps** contiene la **D3DCPCAPS_SOFTWARE** o **D3DCPCAPS_HARDWARE,** el controlador puede realizar el cifrado.
-   El **miembro KeyExchangeType** especifica cómo realizar el intercambio de claves para la clave de sesión.
-   Si el **miembro Caps** contiene la **D3DCPCAPS_CONTENTKEY,** el controlador usa una clave de contenido independiente para el cifrado. Esto es importante cuando se genera la clave de sesión.

Las funcionalidades adicionales se indican en el **miembro Caps.**

### <a name="2-configure-the-authenticated-channel"></a>2. Configuración del canal autenticado

El siguiente paso consiste en configurar el canal autenticado.

1.  Llame [**a IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel) para crear el canal autenticado. Para el *parámetro ChannelType,* especifique un tipo de canal que coincida con las funciones del controlador.
    -   El **D3DAUTHENTICATEDCHANNEL_DRIVER_SOFTWARE** de canal correspondiente a **D3DCPCAPS_SOFTWARE**.
    -   El **D3DAUTHENTICATEDCHANNEL_DRIVER_HARDWARE** de canal correspondiente a **D3DCPCAPS_HARDWARE**.

    El **método CreateAuthenticatedChannel** devuelve un puntero a la interfaz [**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9) junto con un identificador para el canal. El identificador se usa más adelante para asociar la sesión criptográfica al canal autenticado.
2.  Llame [**a IDirect3DAuthenticatedChannel9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize) para obtener el tamaño del certificado X.509 del controlador. Asigne un búfer del tamaño necesario.
3.  Llame [**a IDirect3DAuthenticatedChannel9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate) para obtener el certificado. El método copia el certificado en el búfer asignado en el paso anterior.
4.  Compruebe que microsoft firmó el certificado del controlador y que no se ha revocado.
5.  Obtenga la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Esta clave de sesión se usa para firmar los datos que se envían al canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame [**a IDirect3DAuthenticatedChannel9::NegotiateKeyExchange**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) para enviar la clave de sesión cifrada al controlador.
8.  Inicialice el canal seguro de la siguiente manera:
    1.  Rellene una estructura [**D3DAUTHENTICATEDCHANNEL_CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md) como se describe en la documentación.
    2.  Envíe el [**D3DAUTHENTICATEDCONFIGURE_INITIALIZE**](d3dauthenticatedconfigure-initialize.md) comando mediante una llamada a [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) como se describe en la sección Envío de comandos [de canal autenticados](#sending-authenticated-channel-commands). Este comando contiene los números de secuencia iniciales de los comandos y las consultas que se envían al canal autenticado.
9.  Compruebe el tipo de canal enviando una [**consulta D3DAUTHENTICATEDQUERY_CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) al canal autenticado, como se describe en la sección Envío de consultas de [canal autenticadas.](#sending-authenticated-channel-queries) Compruebe que el tipo de canal coincide con lo que especificó en el [**método CreateAuthenticatedChannel.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel)

### <a name="3-configure-the-cryptographic-session"></a>3. Configurar la sesión criptográfica

A continuación, configure la sesión criptográfica y establezca la clave de sesión.

1.  Llame [**a IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) para crear la sesión criptográfica. Este método devuelve un puntero a la [**interfaz IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9) y junto con un identificador para la sesión criptográfica.
2.  Llame [**a IDirect3DCryptoSession9::GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificatesize) para obtener el tamaño del certificado X.509 del controlador. Asigne un búfer del tamaño necesario.
3.  Llame [**a IDirect3DCryptoSession9::GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dcryptosession9-getcertificate) para obtener el certificado. El método copia el certificado en el búfer asignado en el paso anterior.
4.  Compruebe que microsoft firmó el certificado del controlador y que no se ha revocado.
5.  Obtenga la clave pública del certificado.
6.  Generar una clave de sesión RSA aleatoria. Se trata de una clave de sesión independiente de la clave de sesión del canal autenticado. Cifre la clave de sesión mediante la clave pública del controlador.
7.  Llame [**a IDirect3DCryptoSession9::NegotiateKeyExchange para**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-negotiatekeyexchange) enviar la clave de sesión cifrada al controlador.
8.  Si las funcionalidades de protección de **contenido incluyen D3DCPCAPS_CONTENTKEY**, cree una clave de contenido RSA aleatoria. Se usará más adelante en el proceso de descodización.

### <a name="4-get-a-handle-to-the-dxva-decoder-device"></a>4. Obtener un identificador para el dispositivo descodificador DXVA

Para el paso siguiente, necesitará un identificador para el dispositivo descodificador DXVA. Para obtener este identificador, rellene una DXVA2_DecodeExecuteParams estructura como se muestra a continuación:


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



Establezca el **miembro pExtensionData** de la [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) estructura en la dirección de una [**DXVA2_DecodeExtensionData**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) estructura.

En la [**DXVA2_DecodeExtensionData,**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeextensiondata) establezca el **miembro Function** en **DXVA2_DECODE_GET_DRIVER_HANDLE**. Establezca **pPrivateOutputData en** la dirección de un búfer lo suficientemente grande como para almacenar un **valor HANDLE.** (En el ejemplo anterior, este búfer es la variable *hDecodeDeviceHandle).*

A [**continuación, llame a IDirectXVideoDecoder::Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) y pase la dirección de la [**DXVA2_DecodeExecuteParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodeexecuteparams) estructura. El identificador del descodificador DXVA se devuelve en **pPrivateOutputData**.

### <a name="5-associate-the-dxva-decoder-with-the-cryptographic-session"></a>5. Asociar el descodificador DXVA con la sesión criptográfica

A continuación, asocie el dispositivo descodificador DXVA con el dispositivo Direct3D y la sesión criptográfica, como se muestra a continuación:

1.  Obtenga un identificador para el dispositivo descodificador DXVA, como se describe en la sección anterior.
2.  Obtenga un identificador para el dispositivo Direct3D mediante el envío de una [**D3DAUTHENTICATEDQUERY_DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) consulta al canal autenticado.
3.  Rellene una estructura [**D3DAUTHENTICATEDCHANNEL_CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md) con la siguiente información:
    -   Establezca el **miembro DXVA2DecodeHandle en** el identificador del dispositivo descodificador DXVA.
    -   Establezca el **miembro CryptoSessionHandle** en el identificador de la sesión criptográfica. El método [**IDirect3DDevice9Video::CreateCryptoSession**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createcryptosession) devuelve este identificador.
    -   Establezca el **miembro DeviceHandle** en el identificador del dispositivo Direct3D.
4.  Llame [**a**](d3dauthenticatedconfigure-cryptosession.md) [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) para enviar un D3DAUTHENTICATEDCONFIGURE_CRYPTOSESSION al canal autenticado.

En el diagrama siguiente se muestra el intercambio de identificadores:

![diagrama que muestra cómo está asociado el descodificador dxva a la sesión criptográfica.](images/d3d9video03.png)

El descodificador de software ahora puede usar la clave de sesión criptográfica para cifrar los búferes de vídeo comprimidos. Cada búfer comprimido tendrá su propio vector de inicialización (IV) especificado en el **miembro pvPVPState** de la [**DXVA2_DecodeBufferDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_decodebufferdesc) estructura.

## <a name="sending-authenticated-channel-commands"></a>Envío de comandos de canal autenticados

Se define un conjunto de comandos para configurar el canal autenticado y establecer varias protecciones de contenido. Para obtener una lista de comandos, [vea Content Protection Comandos](content-protection-commands.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es una [**estructura D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT**](d3dauthenticatedchannel-configure-input.md) seguida de campos adicionales. Rellene la estructura **D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT** como se muestra en la tabla siguiente.

    
| Miembro | Descripción | 
|--------|-------------|
| <strong>Omac</strong> | Omita este campo por ahora. | 
| <strong>ConfigureType</strong> | GUID que identifica el comando. Para obtener una lista de comandos, <a href="content-protection-commands.md">vea Content Protection Comandos</a>. | 
| <strong>hChannel</strong> | Identificador del canal autenticado. | 
| <strong>SequenceNumber</strong> | El número de secuencia global. El primer número de secuencia se especifica mediante el envío de <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> comando. Cada vez que envíe otro comando, incremente este número en 1. El número de secuencia protege contra ataques de reproducción.    <blockquote>    [!Note]<br />    Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.    </blockquote><br /><br /> | 


    

     

2.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del **miembro omac** de la estructura de entrada. A continuación, copie este valor de etiqueta en el **miembro omac.**
3.  Llame [**a IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).
4.  El controlador coloca la salida del comando en la [**D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT**](d3dauthenticatedchannel-configure-output.md) estructura.
5.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del **miembro omac** de la estructura de salida. Compare esto con el valor del **miembro omac.** Se producirá un error si no coinciden.
6.  Compare los valores de los **miembros ConfigureType**, **hChannel** y **SequenceNumber** de la estructura de salida con los valores de esos miembros. Se producirá un error si no coinciden.
7.  Incremente el número de secuencia para el comando siguiente.

## <a name="sending-authenticated-channel-queries"></a>Envío de consultas de canal autenticadas

Se define un conjunto de consultas para recuperar información sobre el canal autenticado. Para obtener una lista de consultas, [vea Content Protection Queries](content-protection-queries.md).

Para enviar un comando al canal autenticado, realice los pasos siguientes.

1.  Rellene la estructura de datos de entrada. Esta estructura de datos siempre es [**D3DAUTHENTICATEDCHANNEL_QUERY_INPUT**](d3dauthenticatedchannel-query-input.md) estructura, posiblemente seguida de campos adicionales. Rellene la estructura **D3DAUTHENTICATEDCHANNEL_QUERY_INPUT** como se muestra en la tabla siguiente.

    
| Miembro | Descripción | 
|--------|-------------|
| <strong>Querytype</strong> | GUID que identifica la consulta. Para obtener una lista de consultas, <a href="content-protection-queries.md">vea Content Protection Queries</a>. | 
| <strong>hChannel</strong> | Identificador del canal autenticado. | 
| <strong>SequenceNumber</strong> | El número de secuencia global. El primer número de secuencia se especifica mediante el envío de <a href="d3dauthenticatedconfigure-initialize.md"><strong>D3DAUTHENTICATEDCONFIGURE_INITIALIZE</strong></a> comando. Cada vez que envíe otra consulta, incremente este número en 1. El número de secuencia protege contra ataques de reproducción.    <blockquote>    [!Note]<br />    Se usan dos números de secuencia independientes, uno para los comandos y otro para las consultas.    </blockquote><br /><br /> | 


    

     

2.  Llame [**a IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).
3.  El controlador coloca la salida de la consulta en una [**D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT**](d3dauthenticatedchannel-query-output.md) estructura. Esta estructura va seguida de campos adicionales, según el tipo de consulta.
4.  Calcule la etiqueta OMAC para el bloque de datos que aparece después del **miembro omac** de la estructura de salida. Compare esto con el valor del **miembro omac.** Se producirá un error si no coinciden.
5.  Compare los valores de los **miembros ConfigureType**, **hChannel** y **SequenceNumber** de la estructura de salida con los valores de esos miembros. Se producirá un error si no coinciden.
6.  Incremente el número de secuencia de la siguiente consulta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D 9](direct3d-video-apis.md)
</dt> </dl>

 

 
