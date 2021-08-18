---
title: Wecutil.exe
description: Wecutil.exe es una utilidad Windows Event Collector que permite a un administrador crear y administrar suscripciones a eventos reenviados desde orígenes de eventos remotos que admiten el protocolo WS-Management eventos.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e93e09bc4eed51448b686f0d18f00ecacaacd31d063c4905757d0185128ee64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750975"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe es una utilidad Windows Event Collector que permite a un administrador crear y administrar suscripciones a eventos reenviados desde orígenes de eventos remotos que admiten el protocolo WS-Management eventos. Los comandos, las opciones y los valores de opción no tienen en cuenta las mayúsculas y minúsculas de esta utilidad.

Si recibe un mensaje que dice "El servidor RPC no está disponible" o "La interfaz es desconocida" al intentar ejecutar wecutil, debe iniciar el servicio recopilador de eventos de Windows (wecsvc). Para iniciar wecsvc, en un símbolo del sistema con privilegios elevados, **escriba net start wecsvc**.

## <a name="list-existing-subscriptions"></a>Enumeración de suscripciones existentes

La sintaxis siguiente se usa para enumerar las suscripciones de eventos remotos existentes.

``` syntax
wecutil { es | enum-subscription }
```

Si usa un script para obtener los nombres de las suscripciones de la salida, deberá omitir los caracteres BOM UTF-8 en la primera línea de la salida. El siguiente script muestra un ejemplo de cómo puede omitir los caracteres BOM.

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a>Obtener configuración de suscripción

La sintaxis siguiente se usa para mostrar los datos de configuración de suscripción de eventos remotos.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Obtener parámetros de configuración

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID. \_ DE SUSCRIPCIÓN**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML utilizado para crear la suscripción.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:*VALUE***
</dt> <dd>

Valor que especifica la salida de los datos de configuración de la suscripción. *VALUE* puede ser "XML" o "Terse" y el valor predeterminado es "Terse". Si *VALUE* es "XML", la salida se imprime en formato "XML". Si *VALUE* es "Terse", la salida se imprime en pares nombre-valor.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***
</dt> <dd>

Valor que especifica si la salida está en formato Unicode. *VALUE* puede ser "true" o "false". Si *VALUE* es "true", la salida está en formato Unicode y, si *VALUE* es "false", la salida no está en formato Unicode.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Obtener el estado de tiempo de ejecución de la suscripción

La sintaxis siguiente se usa para mostrar el estado de tiempo de ejecución de la suscripción.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Obtener parámetros de estado

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID. \_ DE SUSCRIPCIÓN**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML utilizado para crear la suscripción.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**ORIGEN DEL \_ EVENTO**
</dt> <dd>

Valor que identifica un equipo que es un origen de eventos para una suscripción de eventos. Este valor puede ser el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP.

</dd> </dl>

## <a name="set-subscription-configuration-information"></a>Establecer la información de configuración de la suscripción

La sintaxis siguiente se usa para establecer los datos de configuración de la suscripción cambiando los parámetros de suscripción desde la línea de comandos o mediante un archivo de configuración XML.

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a>Comentarios

Cuando se especifica un nombre de usuario o una contraseña incorrectos en el comando **wecutil ss,** no se notifica ningún error hasta que se ve el estado en tiempo de ejecución de la suscripción mediante el comando **wecutil gr.**

## <a name="set-configuration-parameters"></a>Establecer parámetros de configuración

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID. \_ DE SUSCRIPCIÓN**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML utilizado para crear la suscripción.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *ARCHIVO DE \_ CONGIG***
</dt> <dd>

Valor que especifica la ruta de acceso al archivo XML que contiene información de configuración de suscripción. La ruta de acceso puede ser absoluta o relativa al directorio actual. Este parámetro solo se puede usar con los parámetros opcionales /cus y /cup, y es mutuamente excluyente con todos los demás parámetros.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***
</dt> <dd>

Valor que determina si se va a habilitar o deshabilitar la suscripción. VALUE puede ser true o false. El valor predeterminado es true, lo que habilita la suscripción.

> [!Note]  
> Cuando se deshabilita una suscripción iniciada por el recopilador, el origen del evento se vuelve inactivo en lugar de deshabilitado. En una suscripción iniciada por el recopilador, puede deshabilitar un origen de eventos independiente de la suscripción.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***
</dt> <dd>

Valor que especifica una descripción para la suscripción de eventos.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE \_ TIME***
</dt> <dd>

Valor que especifica la hora de expiración de la suscripción. *DATE \_ TIME* es un valor especificado en formato de fecha y hora ESTÁNDAR XML o ISO8601: "yyyy-MM-ddThh:mm:ss \[ .sss Z" donde "T" es el separador de hora y \] \[ \] "Z" indica la hora UTC. Por ejemplo, si *DATE \_ TIME* es "2007-01-12T01:20:00", la hora de expiración de la suscripción es el 12 de enero de 2007, 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***
</dt> <dd>

Valor que especifica el tipo de eventos consumidos por la suscripción. La dirección del equipo de origen del evento junto con el identificador uniforme de recursos (URI) identifica de forma única el origen de los eventos. La cadena uri se usa para todas las direcciones de origen de eventos de la suscripción.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *MODO DE \_ CONFIGURACIÓN***
</dt> <dd>

Valor que especifica el modo de configuración de la suscripción de eventos. *CONFIGURACIÓN \_ MODE* puede ser una de las cadenas siguientes: "Normal", "Custom", "MinLatency" o "MinBandwidth". La [**\_ enumeración EC SUBSCRIPTION \_ CONFIGURATION \_ MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) define los modos de configuración. Los parámetros /dm, /dmi, /hi y /dmlt solo se pueden especificar si el modo de configuración está establecido en Personalizado.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***
</dt> <dd>

Valor que especifica la cadena de consulta para la suscripción. El formato de esta cadena puede ser diferente para los distintos valores de URI y se aplica a todos los orígenes de eventos de la suscripción.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***
</dt> <dd>

Valor que especifica el dialecto que usa la cadena de consulta.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***
</dt> <dd>

Valor que especifica el formato de los eventos devueltos. *FORMAT* puede ser "Events" o "RenderedText". Cuando el valor es "RenderedText", los eventos se devuelven con las cadenas localizadas (como cadenas de descripción de eventos) adjuntas a los eventos. El valor predeterminado de *FORMAT* es "RenderedText".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *CONFIGURACIÓN REGIONAL***
</dt> <dd>

Valor que especifica la configuración regional para la entrega de las cadenas localizadas en formato de texto representado. *LOCALE* es un identificador de idioma o referencia cultural de país, por ejemplo, "EN-us". Este parámetro solo es válido cuando el parámetro /cf se establece en "RenderedText".

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree: \[ *VALUE*\]**
</dt> <dd>

Valor que especifica qué eventos se van a entregar para la suscripción. *VALUE* puede ser true o false. Cuando *VALUE es* true, todos los eventos existentes se leen de los orígenes de eventos de suscripción. Cuando *VALUE* es false, solo se entregan eventos futuros (que llegan). El valor predeterminado es true cuando se especifica /ree sin un valor y el valor predeterminado es false si no se especifica /ree.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***
</dt> <dd>

Valor que especifica el registro de eventos local que se usa para almacenar los eventos recibidos de la suscripción de eventos.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***
</dt> <dd>

Valor que especifica el nombre del publicador de eventos (proveedor). Debe ser un publicador que posee o importa el registro especificado por el parámetro /lf.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***
</dt> <dd>

Valor que especifica el modo de entrega de la suscripción. *MODE* puede ser de inserción o extracción. Esta opción solo es válida si el parámetro /cm está establecido en Personalizado.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***
</dt> <dd>

Valor que especifica el número máximo de elementos para la entrega por lotes en la suscripción de eventos. Esta opción solo es válida si el parámetro /cm está establecido en Personalizado.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***
</dt> <dd>

Valor que especifica la latencia máxima permitida para entregar un lote de eventos. MS es el número de milisegundos permitido. Este parámetro solo es válido si el parámetro /cm está establecido en Personalizado.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***
</dt> <dd>

Valor que especifica el intervalo de latido de la suscripción. *MS* es el número de milisegundos usados en el intervalo. Este parámetro solo es válido si el parámetro /cm está establecido en Personalizado.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***
</dt> <dd>

Valor que especifica el nombre del transporte utilizado para conectarse al equipo de origen de eventos remoto.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT \_ SOURCE***
</dt> <dd>

Valor que especifica la dirección de un equipo de origen de eventos. *EVENT \_ SOURCE* es una cadena que identifica un equipo de origen de eventos mediante el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP. Este parámetro se puede usar con los parámetros /ese, /aes, /res o /un y /up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***
</dt> <dd>

Valor que determina si se debe habilitar o deshabilitar un origen de eventos. *VALUE* puede ser true o false. El valor predeterminado es true, que habilita el origen del evento. Este parámetro solo se usa si se usa el parámetro /esa.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Valor que agrega el origen del evento especificado por el parámetro /esa si el origen del evento aún no forma parte de la suscripción de eventos. Si el equipo especificado por el parámetro /esa ya forma parte de la suscripción, se muestra un error. Este parámetro solo se permite si se usa el parámetro /esa.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Valor que quita el origen del evento especificado por el parámetro /esa si el origen del evento ya forma parte de la suscripción de eventos. Si el equipo especificado por el parámetro /esa no forma parte de la suscripción, se muestra un error. Este parámetro solo se permite si se usa el parámetro /esa.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***
</dt> <dd>

Valor que especifica el nombre de usuario utilizado en las credenciales para conectarse al origen del evento especificado en el parámetro /esa. Este parámetro solo se permite si se usa el parámetro /esa.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***
</dt> <dd>

Valor que especifica la contraseña del nombre de usuario especificado en el parámetro /un. Las credenciales de nombre de usuario y contraseña se usan para conectarse al origen de eventos especificado en el parámetro /esa. Este parámetro solo se permite si se usa el parámetro /un.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***
</dt> <dd>

Valor que especifica el número de puerto utilizado por el transporte al conectarse a un equipo de origen de eventos remoto.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***
</dt> <dd>

Valor que especifica el nombre DNS del equipo local. Este nombre lo usan los orígenes de eventos remotos para insertar eventos y solo se debe usar para suscripciones de inserción.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***
</dt> <dd>

Valor que especifica el tipo de credencial utilizado para acceder a orígenes de eventos remotos. *TYPE* puede ser "default", "negotiate", "digest", "basic" o "localmachine". El valor predeterminado es "default". Estos valores se definen en la [**enumeración EC \_ SUBSCRIPTION CREDENTIALS \_ \_ TYPE.**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***
</dt> <dd>

Valor que establece las credenciales de usuario compartidas usadas para los orígenes de eventos que no tienen sus propias credenciales de usuario.

> [!Note]  
> Si este parámetro se usa con la opción /c, se omite la configuración de nombre de usuario y contraseña para orígenes de eventos individuales del archivo de configuración. Si desea usar credenciales diferentes para un origen de eventos específico, puede invalidar este valor especificando los parámetros /un y /up para un origen de eventos específico en la línea de comandos de otro comando set-subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***
</dt> <dd>

Valor que establece la contraseña de usuario para las credenciales de usuario compartidas. Cuando *PASSWORD* se establece en \* (asterisco), la contraseña se lee desde la consola. Esta opción solo es válida cuando se especifica el parámetro /cun.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *HUELLAS DIGITALES***
</dt> <dd>

Valor que establece la lista de huellas digitales del certificado del emisor, en una lista separada por comas.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por origen.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *PERMITIDO***
</dt> <dd>

Valor que establece una lista separada por comas de cadena que especifica los nombres DNS de los equipos que no son de dominio que pueden iniciar suscripciones. Los nombres se pueden especificar mediante caracteres comodín, como \* ".mydomain.com". Esta lista aparece vacía de forma predeterminada.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por origen.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***
</dt> <dd>

Valor que establece una lista separada por comas de cadena que especifica los nombres DNS de los equipos que no son de dominio que no pueden iniciar suscripciones. Los nombres se pueden especificar mediante caracteres comodín, como \* ".mydomain.com". Esta lista aparece vacía de forma predeterminada.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por origen.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***
</dt> <dd>

Valor que establece una cadena, en formato SDDL, que especifica qué equipos de dominio pueden o no iniciar suscripciones. El valor predeterminado es permitir que todos los equipos de dominio inicien suscripciones.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por origen.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Crear una suscripción

La sintaxis siguiente se usa para crear una suscripción de eventos para eventos en un equipo remoto.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Comentarios

Cuando se especifica un nombre de usuario o una contraseña incorrectos en el comando **wecutil cs,** no se notifica ningún error hasta que se ve el estado en tiempo de ejecución de la suscripción mediante el comando **wecutil gr.**

## <a name="creation-parameters"></a>Parámetros de creación

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**ARCHIVO DE \_ CONFIGURACIÓN**
</dt> <dd>

Valor que especifica la ruta de acceso al archivo XML que contiene información de configuración de suscripción. La ruta de acceso puede ser absoluta o relativa al directorio actual.

El siguiente XML es un ejemplo de un archivo de configuración de suscripción que crea una suscripción iniciada por el recopilador para reenviar eventos desde el registro de eventos de aplicación de un equipo remoto al registro ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



El siguiente XML es un ejemplo de un archivo de configuración de suscripción que crea una suscripción iniciada por el origen para reenviar eventos desde el registro de eventos de aplicación de un equipo remoto al registro ForwardedEvents.


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> Al crear una suscripción iniciada por el origen, si **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** IssuerCAList, AllowedSubjectList y DeniedSubjectList están vacíos, se proporciona un valor predeterminado para /  **AllowedSourceDomainComputers:** "O:NSG:NSD:(A;;  GA;;;D C)(A;; GA;;; NS)". Este valor predeterminado de SDDL concede a los miembros del grupo de dominio Equipos de dominio, así como al grupo servicio de red local (para el reenviador local), la capacidad de generar eventos para esta suscripción.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***
</dt> <dd>

Valor que establece las credenciales de usuario compartidas usadas para los orígenes de eventos que no tienen sus propias credenciales de usuario. Este valor solo se aplica a las suscripciones iniciadas por el recopilador.

> [!Note]  
> Si se especifica este parámetro, se omite la configuración de nombre de usuario y contraseña para los orígenes de eventos individuales del archivo de configuración. Si desea usar credenciales diferentes para un origen de eventos específico, puede invalidar este valor especificando los parámetros /un y /up para un origen de eventos específico en la línea de comandos de otro comando set-subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***
</dt> <dd>

Valor que establece la contraseña de usuario para las credenciales de usuario compartidas. Cuando *PASSWORD* se establece en " \* " (asterisco), la contraseña se lee desde la consola. Esta opción solo es válida cuando se especifica el parámetro /cun.

</dd> </dl>

## <a name="delete-a-subscription"></a>Eliminar una suscripción

La sintaxis siguiente se usa para eliminar una suscripción de eventos.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Parámetros de eliminación

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID. \_ DE SUSCRIPCIÓN**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML utilizado para crear la suscripción. Se eliminará la suscripción identificada en este parámetro.

</dd> </dl>

## <a name="retry-a-subscription"></a>Reintentar una suscripción

La sintaxis siguiente se usa para reintentar una suscripción inactiva intentando reactivar todos los orígenes de eventos o especificados estableciendo una conexión a cada origen de eventos y enviando una solicitud de suscripción remota al origen del evento. Los orígenes de eventos deshabilitados no se reinterio.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Parámetros de reintento

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**ID. \_ DE SUSCRIPCIÓN**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML utilizado para crear la suscripción. Se reinterá la suscripción identificada en este parámetro.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**ORIGEN DEL \_ EVENTO**
</dt> <dd>

Valor que identifica un equipo que es un origen de eventos para una suscripción de eventos. Este valor puede ser el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Configuración del servicio Windows recopilador de eventos

La sintaxis siguiente se usa para configurar el servicio Windows Recopilador de eventos para asegurarse de que las suscripciones de eventos se pueden crear y mantener mediante reinicios del equipo. Esto incluye el procedimiento siguiente:

**Para configurar el servicio Windows recopilador de eventos**

1.  Habilite el canal ForwardedEvents si está deshabilitado.
2.  Retrase el inicio del Windows recopilador de eventos.
3.  Inicie el Windows recopilador de eventos si no se está ejecutando.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Configuración de parámetros del recopilador de eventos

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***
</dt> <dd>

Valor que determina si el comando quick-config solicitará confirmación. VALUE puede ser true o false. Si VALUE es true, el comando solicitará confirmación. El valor predeterminado es false.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

 





