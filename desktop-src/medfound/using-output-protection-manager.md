---
description: 'Más información sobre: Uso de Output Protection Manager'
ms.assetid: 01edc17e-e71c-4772-a03c-09c9a2b8400f
title: Uso de Output Protection Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e37dd548603a6f9d7769a9e724df3477e2fcde
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475521"
---
# <a name="using-output-protection-manager"></a>Uso de Output Protection Manager

En este tema se describe cómo usar Output Protection Manager (OPM) para proteger el contenido de vídeo a medida que viaja a través de un conector físico a un dispositivo de visualización. Este tema contiene las siguientes secciones:

-   [Salidas de vídeo](#video-outputs)
-   [Inicialización de una sesión de OPM](#initializing-an-opm-session)
-   [Envío de solicitudes de estado de OPM](#sending-opm-status-requests)
-   [Envío de comandos de OPM](#sending-opm-commands)
-   [Control de una salida de vídeo deshabilitada](#sending-opm-commands)
-   [Uso de HDCP para proteger el contenido](#using-hdcp-to-protect-content)

Premium contenido de vídeo normalmente se cifra para protegerlo contra la duplicación no autorizada. Por supuesto, el vídeo debe descifrarse antes de que se muestre. A continuación, los fotogramas descifrados y sin comprimir deben desplazarse a través de un conector físico al dispositivo de visualización. Los proveedores de contenido pueden requerir que los fotogramas de vídeo estén protegidos en este momento, ya que viajan a través del conector físico.

Existen varios mecanismos de protección para este propósito, incluidos High-Bandwidth Digital Content Protection (HDCP) y DisplayPort Content Protection (DPCP) para salidas digitales. y Sistema de administración de generación de copias: análogo (CGMS-A) para salidas análogas. Por lo general, estos mecanismos implican cifrar o codificar la señal antes de que vaya a la pantalla.

OPM permite que una aplicación aplique mecanismos de protección de contenido en la salida del vídeo. Con OPM, la aplicación envía comandos y solicitudes de estado al controlador de gráficos a través de un canal seguro y de confianza. OPM permite que una aplicación:

-   Compruebe que Microsoft ha firmado un controlador de gráficos.
-   Configure un canal de comunicación de confianza con el controlador.
-   Aplicar mecanismos de protección de contenido en la salida física.

OPM reemplaza a Certified Output Protection Protcol (COPP) y usa una API similar. Para la compatibilidad con versiones anteriores, la interfaz OPM puede emular la interfaz COPP. Entre las diferencias entre OPM y COPP se incluyen las siguientes:

-   OPM usa certificados X.509, mientras que COPP usa un formato de certificado propietario.
-   OPM admite repetidores HDCP.
-   Las aplicaciones que usan OPM no tienen que analizar los mensajes de renovación del sistema (SRE) de HDCP.
-   OPM se puede usar cuando la pantalla de gráficos usa el modo de clonación. COPP no admite el modo de clonación.

Si la aplicación usa la ruta de acceso multimedia protegida (PMP) para reproducir contenido de vídeo, no tiene que usar la API de OPM, ya que el PMP realiza todas las llamadas de OPM necesarias. La API de OPM está disponible para las aplicaciones que no usan el PMP.

OPM está disponible en Windows Vista y versiones posteriores, pero la API no se hizo pública hasta Windows 7. Para usar OPM en una aplicación, debe tener los encabezados y los archivos de biblioteca del SDK Windows 7. No es necesario redistribuir ningún archivo DLL para usar OPM en Windows Vista o Windows Server 2008.

## <a name="video-outputs"></a>Salidas de vídeo

Un adaptador de gráficos puede tener más de una salida física, cada una con sus propias funcionalidades. Antes de que una aplicación reproduce contenido protegido, debe establecer los mecanismos de protección adecuados en cada salida de vídeo asociada a la tarjeta gráfica que mostrará el vídeo. Los mecanismos de protección que se aplicarán dependerán de las reglas de uso del contenido.

Cada salida de vídeo se representa mediante una instancia de la [**interfaz IOPMVideoOutput.**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) Puede usar un dispositivo Direct3D o identificadores de monitor para obtener las salidas de vídeo.

Uso de un dispositivo Direct3D:

1.  Obtenga el **puntero IDirect3DDevice9** para el dispositivo Direct3D que la aplicación usará para crear superficies que contendrán los fotogramas de vídeo.
2.  Llame a [**la función OPMGetVideoOutputsFromIDirect3DDevice9Object.**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) Esta función asigna una matriz de punteros [**IOPMVideoOutput,**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) uno para cada salida.

Uso de identificadores de monitor:

1.  Llame **a EnumDisplayMonitors** para obtener los **identificadores HMONITOR** que corresponden a la ventana de vídeo. Se pueden asociar varios monitores a la misma ventana, por lo que es posible que obtenga varios **identificadores HMONITOR.**
2.  Para cada identificador de monitor, llame [**a OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor). Esta función asigna una matriz de punteros [**IOPMVideoOutput,**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) uno para cada salida.

## <a name="initializing-an-opm-session"></a>Inicialización de una sesión de OPM

Antes de que la aplicación envíe comandos OPM o solicitudes de estado, debe comprobar que la salida del vídeo es de confianza y establecer una clave de sesión. La clave de sesión se usa para firmar los datos que se intercambian entre la aplicación y el controlador de gráficos.

La API de OPM define un protocolo de enlace que establece la confianza y establece la clave de sesión. Debe realizar este protocolo de enlace para cada instancia de la interfaz [**IOPMVideoOutput,**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) como se muestra a continuación:

1.  Llame [**a IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization). Este método recupera dos fragmentos de datos:
    -   Número aleatorio, generado por el controlador. Usará este número para completar el protocolo de enlace.
    -   Cadena de certificados X.509 del controlador.
2.  Compruebe que Microsoft ha firmado la cadena de certificados.
    > [!Note]  
    > La revocación de certificados está fuera del ámbito de OPM.

     

3.  Obtenga la clave pública del controlador de la cadena de certificados.
4.  Generar una clave de sesión AES de 128 bits.
5.  Genere dos números aleatorios de 32 bits:

    -   Número de secuencia inicial para las solicitudes de estado de OPM.
    -   Número de secuencia inicial para los comandos de OPM.

    Estos números deben generarse mediante un generador de números pseudoaleativos seguros criptográficamente, como **CryptGenRandom**.

6.  Copie el número aleatorio del controlador (obtenido en el paso 1), la clave de sesión y los dos números de secuencia en una estructura [**OPM \_ ENCRYPTED INITIALIZATION \_ \_ PARAMETERS,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) como se describe en [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).
7.  Cifre [**la estructura OPM ENCRYPTED INITIALIZATION \_ \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters) con RSAES-OAEP, mediante la clave pública del controlador, que se encuentra en el certificado del controlador.
8.  Llame [**a IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization).

## <a name="sending-opm-status-requests"></a>Envío de solicitudes de estado de OPM

Las solicitudes de estado de OPM devuelven información sobre la salida de vídeo, como el tipo de conector físico y el nivel de protección actual. Para obtener una lista de tipos de solicitud, vea [Solicitudes de estado de OPM](opm-status-requests.md).

Para enviar una solicitud de estado, realice los pasos siguientes.

1.  Inicialice una [**estructura OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) como se muestra en la tabla siguiente.

    | Miembro               | Descripción                                                                                                                                                                                                                                                                                                                                                                 |
    |----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Omac**             | Omita este campo por ahora.                                                                                                                                                                                                                                                                                                                                                    |
    | **rnRandomNumber**   | Número aleatorio de 128 bits seguro criptográficamente. Siempre que realice una solicitud de estado, genere siempre un nuevo número aleatorio, incluso si realiza la misma solicitud. Almacene el número en una variable, ya que tendrá que hacer referencia a él más adelante.                                                                                                                             |
    | **guidInformation**  | GUID que identifica la solicitud de estado. Para obtener una lista de solicitudes de estado, vea [Solicitudes de estado de OPM](opm-status-requests.md).                                                                                                                                                                                                                                               |
    | **ulSequenceNumber** | El número de secuencia global. Para la primera solicitud de estado, use el número de secuencia inicial que especificó en el método [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (paso 5 de Inicialización de una sesión [de OPM).](#initializing-an-opm-session) Cada vez que realice otra solicitud de estado, incremente este número en 1. |
    | **abParameters**     | Matriz de bytes que contiene datos de entrada adicionales para la solicitud. El formato de los datos de entrada se muestra en el tema de referencia para cada solicitud de estado.                                                                                                                                                                                                                    |
    | **cbParametersSize** | Tamaño de los datos válidos en la **matriz abParameters.** El contenido del resto de la matriz no está definido.                                                                                                                                                                                                                                                              |

    

     

2.  Calcule el mac de CBC de una clave (OMAC-1) para calcular un hash para el bloque de datos que aparece después del miembro **omac** y, a continuación, establezca el miembro **omac** en este valor. Vea [Código de ejemplo de OPM](opm-example-code.md).
3.  Llame al [**método IOPMVideoOutput::GetInformation.**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) Pase un puntero a la estructura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) y un puntero a una [**estructura OPM REQUESTED \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) La respuesta del controlador se escribe en la **estructura OPM \_ REQUESTED \_ INFORMATION.**
    -   El **miembro omac** de esta estructura contiene un OMAC calculado para los datos que siguen a este miembro.
    -   El **miembro abRequestedInformation** es una matriz de bytes que contiene los datos de salida de la respuesta. El formato de los datos de salida se muestra en el tema de referencia de cada solicitud de estado.
4.  Calcule un OMAC para la [**estructura \_ OPM REQUESTED \_ INFORMATION,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) sin incluir el **miembro omac.** Compruebe que OMAC coincide con el valor del **miembro omac.**
5.  Asegúrese de que **el miembro cbRequestedInformationSize** de la estructura [**OPM REQUESTED \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) proporciona el tamaño correcto para los datos de salida. Por ejemplo, los datos de salida de la consulta [**OPM \_ GET CONNECTOR \_ \_ TYPE**](opm-get-connector-type.md) son una estructura [**OPM STANDARD \_ \_ INFORMATION,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) por lo que el valor de **cbRequestedInformationSize** debe ser `sizeof(OPM_STANDARD_INFORMATION)` .
6.  Convierte el **miembro abRequestedInformation** de la estructura [**OPM \_ REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) en la estructura de datos de salida correcta. Por ejemplo, si la solicitud de estado es [**OPM \_ GET CONNECTOR \_ \_ TYPE**](opm-get-connector-type.md), **cast abRequestedInformation** a una [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
7.  Asegúrese de que el **miembro rnRandomNumber** de la estructura de datos de salida coincide con el valor de **rnRandomNumber** del paso 1.
8.  Compruebe el **miembro ulStatusFlags** de la estructura de datos de salida, como se describe en [Control de una salida de vídeo deshabilitada.](#handling-a-disabled-video-output)

Si se produce un error en cualquiera de las comprobaciones de los pasos 5 a 8, la aplicación debe dejar de mostrar contenido protegido.

## <a name="sending-opm-commands"></a>Envío de comandos de OPM

Los comandos de OPM se usan para establecer el nivel de protección y otras opciones en la salida del vídeo. El envío de un comando OPM es similar al envío de una solicitud de estado, salvo que no hay datos de respuesta del controlador. Para obtener una lista de comandos, vea [Comandos de OPM](opm-commands.md).

Para enviar un comando OPM, realice los pasos siguientes.

1.  Rellene una estructura [**OPM \_ CONFIGURE \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) como se muestra en la tabla siguiente.

    | Miembro                | Descripción                                                                                                                                                                                                                                                                                                                                                   |
    |-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **Omac**              | Omita este campo por ahora.                                                                                                                                                                                                                                                                                                                                      |
    | **guidSetting**       | GUID que identifica el comando. Para obtener una lista de comandos, vea [Comandos de OPM](opm-commands.md).                                                                                                                                                                                                                                                             |
    | **ulSequenceNumber**  | El número de secuencia global. Para el primer comando, use el número de secuencia inicial que especificó en el método [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) (paso 5 de Inicialización de una sesión [de OPM).](#initializing-an-opm-session) Cada vez que envíe otro comando, incremente este número en 1. |
    | **abParameters**      | Matriz de bytes que contiene datos de entrada adicionales para el comando. El formato de los datos de entrada se muestra en el tema de referencia de cada comando.                                                                                                                                                                                                             |
    | **cbSettingDataSize** | Tamaño de los datos válidos en la **matriz abParameters.** El contenido del resto de la matriz no está definido.                                                                                                                                                                                                                                                |

    

     

2.  Calcule un OMAC para el bloque de datos que aparece después del miembro **omac** y, a continuación, establezca el **miembro omac** en este valor.
3.  Llame [**a IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).

Para la mayoría de los comandos, hay una solicitud de estado correspondiente que devuelve el estado del comando. Por ejemplo, el comando [**OPM \_ SET PROTECTION \_ \_ LEVEL**](opm-set-protection-level.md) establece el nivel de protección y el comando [**OPM GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) obtiene el nivel de protección actual.

## <a name="handling-a-disabled-video-output"></a>Control de una salida de vídeo deshabilitada

Una salida de vídeo puede deshabilitarse en cualquier momento para evitar el uso no autorizado de contenido de vídeo. Esto puede ocurrir porque un mecanismo de protección deja de funcionar, porque el controlador detecta la manipulación o porque la pantalla se desconectó del conector físico. Mientras una salida de vídeo está deshabilitada, no se muestran fotogramas de vídeo.

Mientras la protección de contenido está habilitada, una aplicación debe realizar periódicamente (al menos una vez cada 2 segundos) los pasos siguientes.

1.  Llame [**a IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) para enviar la solicitud de estado [**OPM GET ACTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-actual-protection-level.md) o [**OPM GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL.**](opm-get-virtual-protection-level.md) Los datos devueltos para ambos comandos son una [**estructura OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)
2.  Compruebe el **miembro ulInformation** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Este miembro contiene una marca que indica si la protección de contenido todavía está habilitada. Si la protección de contenido está desactivada, deje de reproducir el vídeo inmediatamente.
3.  Si la protección de contenido está activo, compruebe el **miembro ulStatusFlags** de la [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) Si no se establece ninguna marca, la salida del vídeo funciona correctamente. De lo contrario, la salida del vídeo está deshabilitada.

Las marcas siguientes se definen para **ulStatusFlags**.




| Marca | Descripción | 
|------|-------------|
| <strong>OPM_STATUS_LINK_LOST</strong> | La protección de salida dejó de funcionar por algún motivo; Por ejemplo, el dispositivo de visualización podría desconectarse del conntector. Detenga la reproducción y desactive todos los mecanismos de protección de salida. | 
| <strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong> | La aplicación debe restablecer la sesión de OPM. Responda como se muestra a continuación:<ol><li>Detenga la reproducción.</li><li>Desactive todos los mecanismos de protección.</li><li>Libere la <a href="/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput"><strong>interfaz IOPMVideoOutput.</strong></a></li><li>Vuelva a crear todas las superficies de vídeo.</li><li>Cree un nuevo objeto OPM e intente restablecer la protección de contenido. Si se produce un error, muestre un mensaje de error al usuario. No reprodgue más contenido de vídeo.</li></ol> | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | Esta marca solo se aplica cuando se usa HDCP e indica la presencia de un dispositivo HDCP revocado. Detenga la reproducción y desactive todos los mecanismos de protección en esta salida de vídeo. Cuando se establece esta marca, <strong>también se OPM_STATUS_LINK_LOST</strong> la marca de OPM_STATUS_LINK_LOST marca. | 
| <strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong> | El controlador ha detectado manipulaciones. Detenga la reproducción y no reprodgue más vídeo con esta salida de vídeo. También es una buena idea dejar de usar cualquier otra salida de vídeo, ya que el sistema podría estar en peligro. | 




 

## <a name="using-hdcp-to-protect-content"></a>Uso de HDCP para proteger el contenido

En esta sección se describe cómo habilitar la protección de salida de HDCP mediante OPM. Este es un esquema general de los pasos que debe seguir la aplicación. Más adelante en esta sección se proporciona información detallada.

1.  Es posible que la aplicación tenga que proporcionar un SRM a la salida del vídeo. El mecanismo para recibir SRE está fuera del ámbito de la interfaz OPM. Por ejemplo, las SRE se pueden entregar como parte de una secuencia de difusión.
2.  La aplicación habilita la protección de salida de HDCP.
3.  La aplicación reproduce el contenido del vídeo. Periódicamente, la aplicación sondea el controlador para asegurarse de que HDCP está activada.
4.  Una vez completada la reproducción, la aplicación desactiva HDCP.

### <a name="setting-the-srm"></a>Establecimiento del SRM

Para establecer el SRM, realice los pasos siguientes.

1.  Inicialice una [**estructura OPM \_ SET \_ HDCP \_ SRM \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters) con el número de versión de SRM.
2.  Almacene el SRM en una variable.
3.  Envíe un [**comando OPM \_ SET \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) a la salida del vídeo. Use el procedimiento descrito en [Envío de comandos de OPM](#sending-opm-commands).
    -   El **miembro abParameters** de la estructura [**OPM CONFIGURE \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) contiene la estructura [**OPM SET \_ \_ HDCP \_ SRM \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)
    -   El *parámetro pbAdditionalParameters* del método [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) apunta a la variable que contiene el SRM.
4.  Envíe una solicitud [**de estado GET CURRENT \_ \_ \_ HDCP \_ SRM \_ VERSION**](opm-get-current-hdcp-srm-version.md) de OPM a la salida del vídeo. Use el procedimiento descrito en [Envío de solicitudes de estado de OPM](#sending-opm-status-requests). Esta solicitud de estado no tiene datos de entrada, por lo que el contenido del **miembro abParameters** de la [**estructura OPM GET INFO \_ \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) no está definido.
5.  Cuando se devuelve el método [**IOPMVideoOutput::GetInformation,**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) la matriz **abRequestedInformation** de la estructura [**OPM \_ REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una estructura [**OPM \_ STANDARD \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El **miembro ulInformation** de esta estructura contiene el número de versión del SRM actual. Este valor debe ser igual al valor del paso 2.

### <a name="enabling-hdcp"></a>Habilitación de HDCP

Para habilitar HDCP, realice los pasos siguientes.

1.  Inicialice una [**estructura OPM \_ SET PROTECTION \_ LEVEL \_ \_ PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) con los valores siguientes:
    -   **ulProtectionType**  =  **OPM \_ TIPO \_ DE PROTECCIÓN \_ HDCP**
    -   **ulProtectionLevel**  =  **OPM \_ HDCP \_ ON**
    -   **Reservado** = 0
    -   **Reserved2** = 0
2.  Envíe un [**comando OPM \_ SET PROTECTION \_ \_ LEVEL.**](opm-set-protection-level.md) Los datos de entrada de la **matriz abParameters** son la [**estructura OPM \_ SET PROTECTION \_ LEVEL \_ \_ PARAMETERS.**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)
3.  Envíe una solicitud [**de estado GET VIRTUAL PROTECTION \_ \_ \_ \_ LEVEL**](opm-get-virtual-protection-level.md) de OPM para comprobar si HDCP está habilitado. Los primeros 4 bytes del **miembro abParameters** de la estructura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) contienen el valor **OPM PROTECTION TYPE \_ \_ \_ HDCP**.

Cuando se [**devuelve el método GetInformation,**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) la matriz **abRequestedInformation** de la estructura [**\_ OPM REQUESTED \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene una [**estructura OPM STANDARD \_ \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) El **miembro ulInformation** de esta estructura contiene un valor de la [**enumeración OPM \_ HDCP PROTECTION \_ \_ LEVEL.**](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) Si el valor es igual a **OPM \_ HDCP \_ ON,** significa que HDCP está habilitado. De lo contrario, repita los pasos del 1 al 2 hasta que HDCP esté habilitado o se produzca un error. (Recuerde incrementar el número de secuencia y generar un nuevo número aleatorio cada vez).

Normalmente se tarda entre 100 y 200 milisegundos en habilitar HDCP, pero puede tardar más. No suponga que HDCP está habilitado hasta que lo haya comprobado.

Cuando la aplicación termine de reproducir contenido protegido, desactive HDCP. Los pasos son los mismos que para habilitar HDCP, pero en el paso 1, **establezca ulProtectionLevel** en **OPM \_ HDCP \_ OFF.**

> [!Note]  
> No habilite HDCP si el tipo de conector es **OPM \_ CONNECTOR TYPE \_ \_ DISPLAYPORT \_ EMBEDDED**. (Vea [**OPM Connector Type Flags**](opm-connector-type-flags.md)[Marcas de tipo de conector de OPM]).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



