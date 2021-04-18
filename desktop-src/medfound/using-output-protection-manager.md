---
description: Más información acerca de cómo usar el administrador de protección de salida
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Usar el administrador de protección de salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bf4def3b0575dd706ae5f0c62924b6f1375a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720484"
---
# <a name="using-output-protection-manager"></a>Usar el administrador de protección de salida

En este tema se describe cómo usar el administrador de protección de salida (OPM) para proteger el contenido de vídeo mientras viaja a través de un conector físico a un dispositivo de pantalla. Este tema contiene las siguientes secciones:

-   [Salidas de vídeo](#video-outputs)
-   [Inicializar una sesión de OPM](#initializing-an-opm-session)
-   [Envío de solicitudes de estado de OPM](#sending-opm-status-requests)
-   [Envío de comandos de OPM](#sending-opm-commands)
-   [Control de una salida de vídeo deshabilitado](#sending-opm-commands)
-   [Usar HDCP para proteger el contenido](#using-hdcp-to-protect-content)

Normalmente, el contenido de vídeo Premium se cifra para protegerlo de la duplicación no autorizada. Por supuesto, el vídeo debe descifrarse antes de que se muestre. Los fotogramas descifrados y sin comprimir deben viajar a través de un conector físico al dispositivo de pantalla. Los proveedores de contenido pueden requerir que los fotogramas de vídeo estén protegidos en este punto, a medida que viajan por el conector físico.

Existen varios mecanismos de protección para este propósito, como High-Bandwidth Digital Content Protection (HDCP) y DisplayPort Content Protection (DPCP) para las salidas digitales; y copie el sistema de administración de generación-analógico (CGMS-A) para salidas analógicas. Por lo general, estos mecanismos implican cifrar o codificar la señal antes de que pase a la pantalla.

OPM permite a una aplicación aplicar mecanismos de protección de contenido en la salida de vídeo. Mediante OPM, la aplicación envía comandos y solicitudes de estado al controlador de gráficos a través de un canal seguro y de confianza. OPM permite a una aplicación:

-   Compruebe que el controlador de gráficos está firmado por Microsoft.
-   Configure un canal de comunicación de confianza con el controlador.
-   Aplique los mecanismos de protección de contenido en la salida física.

OPM reemplaza la protección de la salida certificada protocolo (COPP) y usa una API similar. Por compatibilidad con versiones anteriores, la interfaz OPM puede emular la interfaz COPP. Entre las diferencias entre OPM y COPP se incluyen las siguientes:

-   OPM usa certificados X. 509, mientras que COPP usa un formato de certificado propietario.
-   OPM admite repetidores de HDCP.
-   Las aplicaciones que usan OPM no tienen que analizar los mensajes de renovación del sistema HDCP (SRMs).
-   OPM se puede usar cuando la pantalla de gráficos usa el modo de clonación. COPP no admite el modo de clonación.

Si su aplicación usa la ruta de acceso multimedia protegida (PMP) para reproducir contenido de vídeo, no tiene que usar la API de OPM, porque el PMP realiza todas las llamadas OPM necesarias. La API de OPM está disponible para las aplicaciones que no usan el PMP.

OPM está disponible en Windows Vista y versiones posteriores, pero la API no se hizo pública hasta Windows 7. Para usar OPM en una aplicación, debe tener los encabezados y los archivos de biblioteca del SDK de Windows 7. No es necesario redistribuir los archivos DLL para usar OPM en Windows Vista o Windows Server 2008.

## <a name="video-outputs"></a>Salidas de vídeo

Un adaptador de gráficos puede tener más de una salida física, cada una con sus propias capacidades. Antes de que una aplicación reproduzca contenido protegido, debe establecer los mecanismos de protección adecuados en cada salida de vídeo asociada a la tarjeta gráfica que mostrará el vídeo. Los mecanismos de protección que se aplicarán dependerán de las reglas de uso para el contenido.

Cada salida de vídeo se representa mediante una instancia de la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) . Puede usar un dispositivo Direct3D o controladores de monitor para obtener las salidas de vídeo.

Uso de un dispositivo Direct3D:

1.  Obtiene el puntero **IDirect3DDevice9** para el dispositivo Direct3D que usará la aplicación para crear superficies que contengan los fotogramas de vídeo.
2.  Llame a la función [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) . Esta función asigna una matriz de punteros de [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , uno para cada salida.

Uso de identificadores de monitor:

1.  Llame a **EnumDisplayMonitors** para obtener los identificadores de **HMONITOR** que corresponden a la ventana de vídeo. Se pueden asociar varios monitores a la misma ventana, por lo que puede obtener varios identificadores de **HMONITOR** .
2.  Para cada controlador de monitor, llame a [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Esta función asigna una matriz de punteros de [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , uno para cada salida.

## <a name="initializing-an-opm-session"></a>Inicializar una sesión de OPM

Antes de que la aplicación envíe comandos OPM o solicitudes de estado, debe comprobar que la salida del vídeo es de confianza y establecer una clave de sesión. La clave de sesión se usa para firmar los datos que se intercambian entre la aplicación y el controlador de gráficos.

La API de OPM define un protocolo de enlace que establece la confianza y establece la clave de sesión. Debe realizar este protocolo de enlace para cada instancia de la interfaz [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) , como se indica a continuación:

1.  Llame a [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Este método recupera dos fragmentos de datos:
    -   Número aleatorio generado por el controlador. Usará este número para completar el protocolo de enlace.
    -   La cadena de certificados X. 509 del controlador.
2.  Compruebe que Microsoft ha firmado la cadena de certificados.
    > [!Note]  
    > La revocación de certificados está fuera del ámbito de OPM.

     

3.  Obtiene la clave pública del controlador de la cadena de certificados.
4.  Genere una clave de sesión AES de 128 bits.
5.  Generar dos números de bits 32 aleatorios:

    -   El número de secuencia inicial para solicitudes de estado de OPM.
    -   El número de secuencia inicial para los comandos OPM.

    Estos números se deben generar mediante un generador de números pseudoaleatorios seguro criptográficamente, como **CryptGenRandom**.

6.  Copie el número aleatorio del controlador (obtenido en el paso 1), la clave de sesión y los dos números de secuencia en una estructura de [**\_ \_ \_ parámetros de inicialización cifrada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) , como se describe en [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).
7.  Cifre la estructura de [**\_ \_ \_ parámetros de inicialización cifrada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) con RSAES-OAEP mediante la clave pública del controlador, que se encuentra en el certificado del controlador.
8.  Llame a [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Envío de solicitudes de estado de OPM

Las solicitudes de estado de OPM devuelven información sobre la salida de vídeo, como el tipo de conector físico y el nivel de protección actual. Para obtener una lista de tipos de solicitud, consulte [solicitudes de estado de OPM](opm-status-requests.md).

Para enviar una solicitud de estado, realice los pasos siguientes.

1.  Inicialice una estructura de [**\_ parámetros de obtención de \_ información \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) tal y como se muestra en la tabla siguiente.

    | Miembro               | Descripción                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**             | Omitir este campo por ahora.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Número aleatorio de 128 bits criptográficamente seguro. Siempre que realice una solicitud de estado, genere siempre un nuevo número aleatorio, incluso si realiza la misma solicitud. Almacene el número en una variable, ya que tendrá que hacer referencia a él más adelante.                                                                                                                             |
    | **guidInformation**  | GUID que identifica la solicitud de estado. Para obtener una lista de solicitudes de estado, consulte [solicitudes de estado de OPM](opm-status-requests.md).                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | El número de secuencia global. Para la primera solicitud de estado, use el número de secuencia de inicio que especificó en el método [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (paso 5 de la [inicialización de una sesión de OPM](#initializing-an-opm-session)). Cada vez que realice otra solicitud de estado, incremente este número en 1. |
    | **abParameters**     | Matriz de bytes que contiene datos de entrada adicionales para la solicitud. El formato de los datos de entrada se muestra en el tema de referencia de cada solicitud de estado.                                                                                                                                                                                                                    |
    | **cbParametersSize** | Tamaño de los datos válidos de la matriz **abParameters** . El contenido del resto de la matriz no está definido.                                                                                                                                                                                                                                                              |

    

     

2.  Calcule el CBC MAC de una clave (OMAC-1) para calcular un hash para el bloque de datos que aparece después del miembro **OMAC** y, a continuación, establezca el miembro **OMAC** en este valor. Vea [código de ejemplo de OPM](opm-example-code.md).
3.  Llame al método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) . Pase un puntero a la estructura [**de \_ \_ \_ parámetros de obtención de información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) y un puntero a una estructura de [**\_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) . La respuesta del controlador se escribe en la estructura de **\_ \_ información solicitada de OPM** .
    -   El miembro **OMAC** de esta estructura contiene una OMAC calculada para los datos que siguen a este miembro.
    -   El miembro **abRequestedInformation** es una matriz de bytes que contiene los datos de salida de la respuesta. El formato de los datos de salida se muestra en el tema de referencia de cada solicitud de estado.
4.  Calcula un OMAC para la estructura de [**\_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) , sin incluir el miembro **OMAC** . Compruebe que OMAC coincide con el valor del miembro **OMAC** .
5.  Asegúrese de que el miembro **cbRequestedInformationSize** de la estructura de [**\_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) proporciona el tamaño correcto para los datos de salida. Por ejemplo, los datos de salida de la consulta de [**\_ \_ \_ tipo de conector OPM Get**](opm-get-connector-type.md) son una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) , por lo que el valor de **cbRequestedInformationSize** debe ser `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Convierta el miembro **abRequestedInformation** de la estructura de [**\_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) en la estructura de datos de salida correcta. Por ejemplo, si la solicitud de estado es el [**\_ tipo de \_ conector \_ OPM Get**](opm-get-connector-type.md), convierta **abRequestedInformation** en una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
7.  Asegúrese de que el miembro **rnRandomNumber** de la estructura de datos de salida coincide con el valor de **rnRandomNumber** del paso 1.
8.  Compruebe el miembro **ulStatusFlags** de la estructura de datos de salida, tal como se describe en [controlar una salida de vídeo deshabilitado](#handling-a-disabled-video-output).

Si se produce un error en cualquiera de las comprobaciones en los pasos 5 – 8, la aplicación debe dejar de mostrar contenido protegido.

## <a name="sending-opm-commands"></a>Envío de comandos de OPM

Los comandos OPM se usan para establecer el nivel de protección y otros valores en la salida de vídeo. El envío de un comando OPM es similar a enviar una solicitud de estado, salvo que no hay datos de respuesta del controlador. Para obtener una lista de comandos, consulte [comandos de OPM](opm-commands.md).

Para enviar un comando OPM, realice los pasos siguientes.

1.  Rellene una estructura de [**\_ \_ parámetros de configuración de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) tal y como se muestra en la tabla siguiente.

    | Miembro                | Descripción                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **omac**              | Omitir este campo por ahora.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | GUID que identifica el comando. Para obtener una lista de comandos, consulte [comandos de OPM](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | El número de secuencia global. Para el primer comando, use el número de secuencia inicial que especificó en el método [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (paso 5 de la [inicialización de una sesión OPM](#initializing-an-opm-session)). Cada vez que envíe otro comando, incremente este número en 1. |
    | **abParameters**      | Matriz de bytes que contiene datos de entrada adicionales para el comando. El formato de los datos de entrada se muestra en el tema de referencia de cada comando.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | Tamaño de los datos válidos de la matriz **abParameters** . El contenido del resto de la matriz no está definido.                                                                                                                                                                                                                                                |

    

     

2.  Calcule un OMAC para el bloque de datos que aparece después del miembro **OMAC** y, a continuación, establezca el miembro **OMAC** en este valor.
3.  Llame a [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Para la mayoría de los comandos, hay una solicitud de estado correspondiente que devuelve el estado del comando. Por ejemplo, el [**comando \_ configuración \_ de \_ nivel de protección OPM**](opm-set-protection-level.md) establece el nivel de protección y el comando [**OPM \_ obtener \_ \_ \_ nivel**](opm-get-virtual-protection-level.md) de protección virtual obtiene el nivel de protección actual.

## <a name="handling-a-disabled-video-output"></a>Control de una salida de vídeo deshabilitado

Una salida de vídeo podría deshabilitarse en cualquier momento para evitar el uso no autorizado del contenido de vídeo. Esto puede deberse a que un mecanismo de protección deja de funcionar, porque el controlador detecta alteraciones o porque la pantalla se desconectó del conector físico. Mientras una salida de vídeo está deshabilitada, no se muestran fotogramas de vídeo.

Mientras está habilitada la protección de contenido, una aplicación debe realizar periódicamente (al menos una vez cada 2 segundos) los pasos siguientes.

1.  Llame a [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) para enviar el [**\_ nivel de \_ \_ protección \_ de OPM real**](opm-get-actual-protection-level.md) o la solicitud de estado de [**\_ \_ \_ \_ nivel de protección virtual de OPM**](opm-get-virtual-protection-level.md) . Los datos devueltos para ambos comandos son una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .
2.  Compruebe el miembro **ulInformation** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Este miembro contiene una marca que indica si la protección de contenido todavía está habilitada. Si la protección de contenido está desactivada, detenga la reproducción del vídeo inmediatamente.
3.  Si la protección de contenido está activada, compruebe el miembro **ulStatusFlags** de la estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . Si no se establece ningún marcador, la salida del vídeo funciona correctamente. De lo contrario, la salida de vídeo está deshabilitada.

Se definen las marcas siguientes para **ulStatusFlags**.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Marca</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>OPM_STATUS_LINK_LOST</strong></td>
<td>La protección de la salida dejó de funcionar por algún motivo. por ejemplo, el dispositivo de pantalla podría estar desconectado de conntector. Detenga la reproducción y desactive todos los mecanismos de protección de salida.</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></td>
<td>La aplicación debe restablecer la sesión OPM. Responda de la siguiente manera:
<ol>
<li>Detenga la reproducción.</li>
<li>Desactive todos los mecanismos de protección.</li>
<li>Libere la interfaz <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>IOPMVideoOutput</strong></a> .</li>
<li>Vuelva a crear todas las superficies de vídeo.</li>
<li>Cree un nuevo objeto OPM e intente restablecer la protección de contenido. Si se produce un error, muestra un mensaje de error al usuario. No reproduzca más contenido de vídeo.</li>
</ol></td>
</tr>
<tr class="odd">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>Esta marca solo se aplica cuando se usa HDCP e indica la presencia de un dispositivo HDCP revocado. Detenga la reproducción y desactive todos los mecanismos de protección de esta salida de vídeo. Cuando se establece esta marca, también se establece la marca de <strong>OPM_STATUS_LINK_LOST</strong> .</td>
</tr>
<tr class="even">
<td><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></td>
<td>El controlador ha detectado alteraciones. Detenga la reproducción y no reproduzca más vídeo con esta salida de vídeo. También es una buena idea dejar de usar cualquier otra salida de vídeo, ya que el sistema podría estar en peligro.</td>
</tr>
</tbody>
</table>



 

## <a name="using-hdcp-to-protect-content"></a>Usar HDCP para proteger el contenido

En esta sección se describe cómo habilitar la protección de salida de HDCP mediante OPM. A continuación se muestra una descripción general de los pasos que debe realizar la aplicación. Más adelante en esta sección se proporcionan detalles.

1.  Es posible que la aplicación tenga que proporcionar un SRM a la salida de vídeo. El mecanismo para recibir SRMs está fuera del ámbito de la interfaz OPM. Por ejemplo, SRMs se puede entregar como parte de un flujo de difusión.
2.  La aplicación habilita la protección de salida de HDCP.
3.  La aplicación reproduce el contenido del vídeo. Periódicamente, la aplicación sondea el controlador para asegurarse de que la HDCP está activada.
4.  Una vez completada la reproducción, la aplicación desactiva HDCP.

### <a name="setting-the-srm"></a>Establecimiento de la SRM

Para establecer la SRM, realice los pasos siguientes.

1.  Inicialice una estructura de [**\_ \_ parámetros de \_ SRM \_ set HDCP de configuración**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) con el número de versión de SRM.
2.  Almacene el SRM en una variable.
3.  Envíe un comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) a la salida de vídeo. Siga el procedimiento descrito en [envío de comandos de OPM](#sending-opm-commands).
    -   El miembro **abParameters** de la estructura de [**\_ \_ parámetros de configuración de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contiene la estructura de [**\_ \_ \_ \_ parámetros**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) de la definición de la configuración de HDCP de HDCP.
    -   El parámetro *pbAdditionalParameters* del método [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) apunta a la variable que contiene el SRM.
4.  Envíe una solicitud de estado de versión de la versión de HDCP de la [**\_ \_ \_ \_ \_ versión actual de HDCP**](opm-get-current-hdcp-srm-version.md) en la salida de vídeo. Siga el procedimiento descrito en [envío de solicitudes de estado de OPM](#sending-opm-status-requests). Esta solicitud de estado no tiene datos de entrada, por lo que el contenido del miembro **abParameters** de la estructura de [**parámetros de obtención de \_ \_ información \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) es indefinido.
5.  Cuando el método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) devuelve, la matriz **abRequestedInformation** de la estructura de [**\_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . El miembro **ulInformation** de esta estructura contiene el número de versión del SRM actual. Este valor debe ser igual al valor del paso 2.

### <a name="enabling-hdcp"></a>Habilitar HDCP

Para habilitar HDCP, realice los pasos siguientes.

1.  Inicialice una estructura de [**\_ parámetros de \_ \_ nivel \_ de protección set de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) con los siguientes valores:
    -   **ulProtectionType**  =  **OPM \_ tipo de protección \_ \_ HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ activado**
    -   **Reservado** = 0
    -   **Reserved2** = 0
2.  Envíe un comando de [**nivel de protección de conjunto de OPM \_ \_ \_**](opm-set-protection-level.md) . Los datos de entrada de la matriz **abParameters** son la estructura de [**parámetros de \_ \_ \_ nivel \_ de protección de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .
3.  Envíe una solicitud de estado de [**\_ \_ \_ \_ nivel de protección virtual de OPM**](opm-get-virtual-protection-level.md) para comprobar si se ha habilitado HDCP. Los primeros 4 bytes del miembro **abParameters** de la estructura [**de \_ \_ \_ parámetros de obtención de información de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) contienen el valor de tipo de **\_ protección OPM \_ \_ HDCP**.

Cuando el método [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) devuelve, la matriz **abRequestedInformation** de la estructura de [**\_ \_ información solicitada de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una estructura de [**\_ \_ información estándar de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) . El miembro **ulInformation** de esta estructura contiene un valor de la enumeración de [**\_ \_ \_ nivel de protección OPM HDCP**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) . Si el valor es igual **\_ a la HDCP \_ de OPM activada**, significa que se habilita HDCP. De lo contrario, repita los pasos 1 a 2 hasta que se habilite HDCP o se produzca un error. (Recuerde incrementar el número de secuencia y generar un nuevo número aleatorio cada vez).

Normalmente, se tarda entre 100 y 200 milisegundos en habilitar HDCP, pero puede tardar más tiempo. No suponga que se ha habilitado HDCP hasta que lo haya comprobado.

Cuando la aplicación termine de reproducir contenido protegido, desactive HDCP. Los pasos son los mismos que para habilitar HDCP, pero en el paso 1, establezca **ulProtectionLevel** en la **HDCP de OPM en \_ \_ OFF**.

> [!Note]  
> No habilite HDCP si el tipo de conector es el **tipo de conector de OPM \_ \_ \_ \_ incrustado**. (Consulte las [**marcas de tipo de conector de OPM**](opm-connector-type-flags.md)).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



