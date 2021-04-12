---
title: Wecutil.exe
description: Wecutil.exe es una utilidad del recopilador de eventos de Windows que permite a un administrador crear y administrar suscripciones a eventos reenviados desde orígenes de eventos remotos que admiten el protocolo de WS-Management.
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
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104362395"
---
# <a name="wecutilexe"></a>Wecutil.exe

Wecutil.exe es una utilidad del recopilador de eventos de Windows que permite a un administrador crear y administrar suscripciones a eventos reenviados desde orígenes de eventos remotos que admiten el protocolo de WS-Management. Los comandos, las opciones y los valores de opción no distinguen mayúsculas de minúsculas para esta utilidad.

Si recibe un mensaje que indica "el servidor RPC no está disponible" o "se desconoce la interfaz" al intentar ejecutar wecutil, debe iniciar el servicio Recopilador de eventos de Windows (wecsvc). Para iniciar wecsvc, en un símbolo del sistema con privilegios elevados, escriba **net start wecsvc**.

## <a name="list-existing-subscriptions"></a>Enumerar las suscripciones existentes

La siguiente sintaxis se usa para enumerar las suscripciones de eventos remotos existentes.

``` syntax
wecutil { es | enum-subscription }
```

Si utiliza un script para obtener los nombres de las suscripciones de la salida, tendrá que omitir los caracteres de BOM UTF-8 en la primera línea de la salida. El siguiente script muestra un ejemplo de cómo podría omitir los caracteres de la BOM.

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

La sintaxis siguiente se usa para mostrar los datos de configuración de la suscripción de eventos remotos.

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a>Obtener parámetros de configuración

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.

</dd> <dt>

<span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: * valor***
</dt> <dd>

Valor que especifica la salida de los datos de configuración de la suscripción. El *valor* puede ser "XML" o "conciso" y el valor predeterminado es "conciso". Si el *valor* es "XML", la salida se imprime en formato "XML". Si el *valor* es "conciso", la salida se imprime en pares de nombre y valor.

</dd> <dt>

<span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *valor***
</dt> <dd>

Valor que especifica si la salida está en formato Unicode. El *valor* puede ser "true" o "false". Si el *valor* es "true", la salida está en formato Unicode y si el *valor* es "false", la salida no está en formato Unicode.

</dd> </dl>

## <a name="get-subscription-runtime-status"></a>Obtener estado de tiempo de ejecución de suscripción

La siguiente sintaxis se usa para mostrar el estado de la suscripción en tiempo de ejecución.

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a>Obtener parámetros de estado

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**origen del evento \_**
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

### <a name="remarks"></a>Observaciones

Cuando se especifica un nombre de usuario o una contraseña incorrectos en el comando **wecutil SS** , no se genera ningún error hasta que se ve el estado de tiempo de ejecución de la suscripción mediante el comando **wecutil gr** .

## <a name="set-configuration-parameters"></a>Establecer parámetros de configuración

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.

</dd> <dt>

<span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG \_ archivo***
</dt> <dd>

Valor que especifica la ruta de acceso al archivo XML que contiene la información de configuración de la suscripción. La ruta de acceso puede ser absoluta o relativa al directorio actual. Este parámetro solo se puede usar con los parámetros opcionales/CUS y/Cup y es mutuamente excluyente con todos los demás parámetros.

</dd> <dt>

<span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *valor***
</dt> <dd>

Valor que determina si se va a habilitar o deshabilitar la suscripción. El valor puede ser true o false. El valor predeterminado es true, que habilita la suscripción.

> [!Note]  
> Cuando se deshabilita una suscripción iniciada por el recopilador, el origen del evento pasa a estar inactivo en lugar de deshabilitarse. En una suscripción iniciada por el recopilador, puede deshabilitar un origen de eventos independiente de la suscripción.

 

</dd> <dt>

<span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Descripción***
</dt> <dd>

Valor que especifica una descripción para la suscripción de eventos.

</dd> <dt>

<span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *fecha y \_ hora***
</dt> <dd>

Valor que especifica la hora de expiración de la suscripción. *Fecha \_ TIME* es un valor especificado en el formato de fecha y hora XML estándar o ISO8601: "aaaa-mm-ddThh: mm: SS \[ . SSS \] \[ Z \] ", donde "T" es el separador de hora y "Z" indica la hora UTC. Por ejemplo, si *fecha y \_ hora* es "2007-01-12T01:20:00", la hora de expiración de la suscripción es el 12 de enero de 2007 y 01:20.

</dd> <dt>

<span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/Uri: *URI***
</dt> <dd>

Valor que especifica el tipo de eventos utilizados por la suscripción. La dirección del equipo de origen del evento junto con el identificador uniforme de recursos (URI) identifica de forma única el origen de los eventos. La cadena URI se usa para todas las direcciones de origen de eventos de la suscripción.

</dd> <dt>

<span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ modo de configuración***
</dt> <dd>

Valor que especifica el modo de configuración de la suscripción de eventos. *Configuración \_ de El modo* puede ser una de las cadenas siguientes: "normal", "Custom", "MinLatency" o "MinBandwidth". La enumeración de modo de configuración de suscripción de EC define los modos de configuración. [**\_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) Los parámetros/DM,/DMI,/HI y/dmlt solo se pueden especificar si el modo de configuración está establecido en Custom.

</dd> <dt>

<span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *consulta***
</dt> <dd>

Valor que especifica la cadena de consulta de la suscripción. El formato de esta cadena puede ser diferente para los distintos valores de URI y se aplica a todos los orígenes de eventos de la suscripción.

</dd> <dt>

<span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/DIA: *dialecto***
</dt> <dd>

Valor que especifica el dialecto que usa la cadena de consulta.

</dd> <dt>

<span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *formato***
</dt> <dd>

Valor que especifica el formato de los eventos devueltos. El *formato* puede ser "Events" o "RenderedText". Cuando el valor es "RenderedText", los eventos se devuelven con las cadenas localizadas (por ejemplo, cadenas de descripción de eventos) adjuntas a los eventos. El valor predeterminado de *Format* es "RenderedText".

</dd> <dt>

<span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *configuración regional***
</dt> <dd>

Valor que especifica la configuración regional para la entrega de las cadenas localizadas en formato de texto representado. La *configuración regional* es un identificador de referencia cultural de idioma o país, por ejemplo, "en-US". Este parámetro solo es válido cuando el parámetro/CF se establece en "RenderedText".

</dd> <dt>

<span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree: \[ *valor*\]**
</dt> <dd>

Valor que especifica los eventos que se van a entregar para la suscripción. El *valor* puede ser true o false. Cuando el *valor* es true, todos los eventos existentes se leen de los orígenes de eventos de suscripción. Cuando el *valor* es false, solo se entregan los eventos futuros (llegados). El valor predeterminado es true cuando se especifica/REE sin un valor, y el valor predeterminado es false si no se especifica/REE.

</dd> <dt>

<span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *nombre de archivo***
</dt> <dd>

Valor que especifica el registro de eventos local que se usa para almacenar los eventos recibidos de la suscripción de eventos.

</dd> <dt>

<span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *publicador***
</dt> <dd>

Valor que especifica el nombre del publicador de eventos (proveedor). Debe ser un publicador que posea o importe el registro especificado por el parámetro/LF.

</dd> <dt>

<span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *modo***
</dt> <dd>

Valor que especifica el modo de entrega de la suscripción. El *modo* puede ser de inserción o de extracción. Esta opción solo es válida si el parámetro/cm está establecido en Custom.

</dd> <dt>

<span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *número***
</dt> <dd>

Valor que especifica el número máximo de elementos para la entrega por lotes en la suscripción de eventos. Esta opción solo es válida si el parámetro/cm está establecido en Custom.

</dd> <dt>

<span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***
</dt> <dd>

Valor que especifica la latencia máxima permitida para entregar un lote de eventos. MS es el número de milisegundos permitidos. Este parámetro solo es válido si el parámetro/cm está establecido en Custom.

</dd> <dt>

<span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/HI: *MS***
</dt> <dd>

Valor que especifica el intervalo de latido de la suscripción. *MS* es el número de milisegundos usados en el intervalo. Este parámetro solo es válido si el parámetro/cm está establecido en Custom.

</dd> <dt>

<span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *nombredetransportedered***
</dt> <dd>

Valor que especifica el nombre del transporte utilizado para conectarse al equipo de origen de eventos remotos.

</dd> <dt>

<span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *\_ origen del evento***
</dt> <dd>

Valor que especifica la dirección de un equipo de origen de eventos. *Evento \_ de ORIGEN* es una cadena que identifica un equipo de origen de eventos con el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP. Este parámetro se puede utilizar con los parámetros/ese,/AES,/res o/un y/up.

</dd> <dt>

<span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *valor***
</dt> <dd>

Valor que determina si se va a habilitar o deshabilitar un origen de eventos. El *valor* puede ser true o false. El valor predeterminado es true, que habilita el origen del evento. Este parámetro solo se usa si se usa el parámetro/esa.

</dd> <dt>

<span id="_aes"></span><span id="_AES"></span>**/aes**
</dt> <dd>

Valor que agrega el origen de eventos especificado por el parámetro/esa si el origen del evento aún no forma parte de la suscripción de eventos. Si el equipo especificado por el parámetro/esa ya forma parte de la suscripción, se muestra un error. Este parámetro solo se permite si se usa el parámetro/esa.

</dd> <dt>

<span id="_res"></span><span id="_RES"></span>**/res**
</dt> <dd>

Valor que quita el origen de eventos especificado por el parámetro/esa si el origen del evento ya forma parte de la suscripción de eventos. Si el equipo especificado por el parámetro/esa no forma parte de la suscripción, se muestra un error. Este parámetro solo se permite si se usa el parámetro/esa.

</dd> <dt>

<span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *nombre de usuario***
</dt> <dd>

Valor que especifica el nombre de usuario usado en las credenciales para conectarse al origen de eventos especificado en el parámetro/esa. Este parámetro solo se permite si se usa el parámetro/esa.

</dd> <dt>

<span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *contraseña***
</dt> <dd>

Valor que especifica la contraseña para el nombre de usuario especificado en el parámetro/un. Las credenciales de nombre de usuario y contraseña se usan para conectarse al origen de eventos especificado en el parámetro/esa. Este parámetro solo se permite si se usa el parámetro/un.

</dd> <dt>

<span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *TRANSPORTPORT***
</dt> <dd>

Valor que especifica el número de puerto utilizado por el transporte al conectarse a un equipo de origen de eventos remoto.

</dd> <dt>

<span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *nombre***
</dt> <dd>

Valor que especifica el nombre DNS del equipo local. Los orígenes de eventos remotos usan este nombre para volver a enviar eventos y deben usarse solo para suscripciones de extracción.

</dd> <dt>

<span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *tipo***
</dt> <dd>

Valor que especifica el tipo de credencial utilizado para tener acceso a los orígenes de eventos remotos. El *tipo* puede ser "default", "Negotiate", "Digest", "Basic" o "LocalMachine". El valor predeterminado es "default". Estos valores se definen en la enumeración de [**\_ \_ \_ tipo de credenciales de suscripción de EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nombre de usuario***
</dt> <dd>

Valor que establece las credenciales de usuario compartidas que se usan para los orígenes de eventos que no tienen sus propias credenciales de usuario.

> [!Note]  
> Si este parámetro se usa con la opción/c, se omite la configuración de nombre de usuario y contraseña para los orígenes de eventos individuales del archivo de configuración. Si desea usar credenciales diferentes para un origen de eventos específico, puede invalidar este valor especificando los parámetros/un y/up para un origen de eventos específico en la línea de comandos de otro comando set-subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *contraseña***
</dt> <dd>

Valor que establece la contraseña de usuario para las credenciales de usuario compartidas. Cuando *contraseña* está establecida en \* (asterisco), la contraseña se lee desde la consola. Esta opción solo es válida cuando se especifica el parámetro/cun.

</dd> <dt>

<span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: *huellas digitales***
</dt> <dd>

Valor que establece la lista de impresiones en miniatura del certificado del emisor, en una lista separada por comas.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por el origen.

 

</dd> <dt>

<span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *permitido***
</dt> <dd>

Valor que establece una lista separada por comas de cadena que especifica los nombres DNS de los equipos que no son de dominio y que pueden iniciar suscripciones. Los nombres se pueden especificar mediante caracteres comodín, como " \* . mydomain.com". Esta lista aparece vacía de forma predeterminada.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por el origen.

 

</dd> <dt>

<span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *denegado***
</dt> <dd>

Valor que establece una lista separada por comas de cadena que especifica los nombres DNS de los equipos que no son de dominio y a los que no se les permite iniciar suscripciones. Los nombres se pueden especificar mediante caracteres comodín, como " \* . mydomain.com". Esta lista aparece vacía de forma predeterminada.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por el origen.

 

</dd> <dt>

<span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***
</dt> <dd>

Valor que establece una cadena, en formato SDDL, que especifica qué equipos del dominio están permitidos o no para iniciar suscripciones. El valor predeterminado es permitir que todos los equipos del dominio inicien las suscripciones.

> [!Note]  
> Esta opción es específica solo para las suscripciones iniciadas por el origen.

 

</dd> </dl>

## <a name="create-a-new-subscription"></a>Crear una suscripción

La siguiente sintaxis se usa para crear una suscripción de eventos para eventos en un equipo remoto.

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a>Observaciones

Cuando se especifica un nombre de usuario o una contraseña incorrectos en el comando **wecutil CS** , no se genera ningún error hasta que se ve el estado de tiempo de ejecución de la suscripción mediante el comando **wecutil gr** .

## <a name="creation-parameters"></a>Parámetros de creación

<dl> <dt>

<span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**archivo de configuración \_**
</dt> <dd>

Valor que especifica la ruta de acceso al archivo XML que contiene la información de configuración de la suscripción. La ruta de acceso puede ser absoluta o relativa al directorio actual.

El siguiente código XML es un ejemplo de un archivo de configuración de suscripción que crea una suscripción iniciada por el recopilador para reenviar eventos del registro de eventos de aplicación de un equipo remoto al registro Eventos reenviados.


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



El siguiente código XML es un ejemplo de un archivo de configuración de suscripción que crea una suscripción iniciada por el origen para reenviar eventos del registro de eventos de aplicación de un equipo remoto al registro Eventos reenviados.


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
> Al crear una suscripción iniciada por el origen, si **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** y **DeniedSubjectList** están todos vacíos, se proporcionará un valor predeterminado para **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; GA;;; NS) ". Este valor predeterminado de SDDL concede a los miembros del grupo de dominio equipos del dominio, así como al grupo servicio de red local (para el reenviador local), la capacidad de generar eventos para esta suscripción.

 

</dd> <dt>

<span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nombre de usuario***
</dt> <dd>

Valor que establece las credenciales de usuario compartidas que se usan para los orígenes de eventos que no tienen sus propias credenciales de usuario. Este valor solo se aplica a las suscripciones iniciadas por el recopilador.

> [!Note]  
> Si se especifica este parámetro, se omite la configuración de nombre de usuario y contraseña para los orígenes de eventos individuales del archivo de configuración. Si desea usar credenciales diferentes para un origen de eventos específico, puede invalidar este valor especificando los parámetros/un y/up para un origen de eventos específico en la línea de comandos de otro comando set-subscription.

 

</dd> <dt>

<span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *contraseña***
</dt> <dd>

Valor que establece la contraseña de usuario para las credenciales de usuario compartidas. Cuando *password* se establece en " \* " (asterisco), la contraseña se lee desde la consola. Esta opción solo es válida cuando se especifica el parámetro/cun.

</dd> </dl>

## <a name="delete-a-subscription"></a>Eliminar una suscripción

La siguiente sintaxis se usa para eliminar una suscripción de eventos.

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a>Parámetros de eliminación

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción. Se eliminará la suscripción identificada en este parámetro.

</dd> </dl>

## <a name="retry-a-subscription"></a>Reintentar una suscripción

La sintaxis siguiente se usa para reintentar una suscripción inactiva intentando reactivar todos los orígenes de eventos o especificados estableciendo una conexión a cada origen de eventos y enviando una solicitud de suscripción remota al origen de eventos. Los orígenes de eventos deshabilitados no se reintentan.

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a>Parámetros de reintento

<dl> <dt>

<span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**
</dt> <dd>

Cadena que identifica de forma única una suscripción. Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción. Se volverá a intentar la suscripción identificada en este parámetro.

</dd> <dt>

<span id="EVENT_SOURCE"></span><span id="event_source"></span>**origen del evento \_**
</dt> <dd>

Valor que identifica un equipo que es un origen de eventos para una suscripción de eventos. Este valor puede ser el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP.

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a>Configurar el servicio Recopilador de eventos de Windows

La siguiente sintaxis se utiliza para configurar el servicio Recopilador de eventos de Windows para garantizar que las suscripciones de eventos se puedan crear y mantener a través de reinicios del equipo. Esto incluye el siguiente procedimiento:

**Para configurar el servicio Recopilador de eventos de Windows**

1.  Habilite el canal de eventos reenviados si está deshabilitado.
2.  Retrasar el inicio del servicio Recopilador de eventos de Windows.
3.  Inicie el servicio Recopilador de eventos de Windows si no se está ejecutando.

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a>Configurar parámetros del recopilador de eventos

<dl> <dt>

<span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *valor***
</dt> <dd>

Un valor que determina si el comando de configuración rápida solicitará confirmación. El valor puede ser true o false. Si el valor es true, el comando solicitará confirmación. El valor predeterminado es false.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

 





