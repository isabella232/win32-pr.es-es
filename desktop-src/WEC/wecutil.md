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
# <a name="wecutilexe"></a><span data-ttu-id="453fa-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="453fa-104">Wecutil.exe</span></span>

<span data-ttu-id="453fa-105">Wecutil.exe es una utilidad del recopilador de eventos de Windows que permite a un administrador crear y administrar suscripciones a eventos reenviados desde orígenes de eventos remotos que admiten el protocolo de WS-Management.</span><span class="sxs-lookup"><span data-stu-id="453fa-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="453fa-106">Los comandos, las opciones y los valores de opción no distinguen mayúsculas de minúsculas para esta utilidad.</span><span class="sxs-lookup"><span data-stu-id="453fa-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="453fa-107">Si recibe un mensaje que indica "el servidor RPC no está disponible" o "se desconoce la interfaz" al intentar ejecutar wecutil, debe iniciar el servicio Recopilador de eventos de Windows (wecsvc).</span><span class="sxs-lookup"><span data-stu-id="453fa-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="453fa-108">Para iniciar wecsvc, en un símbolo del sistema con privilegios elevados, escriba **net start wecsvc**.</span><span class="sxs-lookup"><span data-stu-id="453fa-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="453fa-109">Enumerar las suscripciones existentes</span><span class="sxs-lookup"><span data-stu-id="453fa-109">List existing subscriptions</span></span>

<span data-ttu-id="453fa-110">La siguiente sintaxis se usa para enumerar las suscripciones de eventos remotos existentes.</span><span class="sxs-lookup"><span data-stu-id="453fa-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="453fa-111">Si utiliza un script para obtener los nombres de las suscripciones de la salida, tendrá que omitir los caracteres de BOM UTF-8 en la primera línea de la salida.</span><span class="sxs-lookup"><span data-stu-id="453fa-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="453fa-112">El siguiente script muestra un ejemplo de cómo podría omitir los caracteres de la BOM.</span><span class="sxs-lookup"><span data-stu-id="453fa-112">The following script shows an example of how you might skip the BOM characters.</span></span>

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

## <a name="get-subscription-configuration"></a><span data-ttu-id="453fa-113">Obtener configuración de suscripción</span><span class="sxs-lookup"><span data-stu-id="453fa-113">Get subscription configuration</span></span>

<span data-ttu-id="453fa-114">La sintaxis siguiente se usa para mostrar los datos de configuración de la suscripción de eventos remotos.</span><span class="sxs-lookup"><span data-stu-id="453fa-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="453fa-115">Obtener parámetros de configuración</span><span class="sxs-lookup"><span data-stu-id="453fa-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-117">Cadena que identifica de forma única una suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="453fa-118">Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: \* valor**\*</span><span class="sxs-lookup"><span data-stu-id="453fa-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="453fa-120">Valor que especifica la salida de los datos de configuración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="453fa-121">El *valor* puede ser "XML" o "conciso" y el valor predeterminado es "conciso".</span><span class="sxs-lookup"><span data-stu-id="453fa-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="453fa-122">Si el *valor* es "XML", la salida se imprime en formato "XML".</span><span class="sxs-lookup"><span data-stu-id="453fa-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="453fa-123">Si el *valor* es "conciso", la salida se imprime en pares de nombre y valor.</span><span class="sxs-lookup"><span data-stu-id="453fa-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *valor***</span><span class="sxs-lookup"><span data-stu-id="453fa-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-125">Valor que especifica si la salida está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="453fa-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="453fa-126">El *valor* puede ser "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="453fa-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="453fa-127">Si el *valor* es "true", la salida está en formato Unicode y si el *valor* es "false", la salida no está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="453fa-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="453fa-128">Obtener estado de tiempo de ejecución de suscripción</span><span class="sxs-lookup"><span data-stu-id="453fa-128">Get subscription runtime status</span></span>

<span data-ttu-id="453fa-129">La siguiente sintaxis se usa para mostrar el estado de la suscripción en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="453fa-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="453fa-130">Obtener parámetros de estado</span><span class="sxs-lookup"><span data-stu-id="453fa-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-132">Cadena que identifica de forma única una suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="453fa-133">Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**origen del evento \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-135">Valor que identifica un equipo que es un origen de eventos para una suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="453fa-136">Este valor puede ser el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="453fa-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="453fa-137">Establecer la información de configuración de la suscripción</span><span class="sxs-lookup"><span data-stu-id="453fa-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="453fa-138">La sintaxis siguiente se usa para establecer los datos de configuración de la suscripción cambiando los parámetros de suscripción desde la línea de comandos o mediante un archivo de configuración XML.</span><span class="sxs-lookup"><span data-stu-id="453fa-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

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

### <a name="remarks"></a><span data-ttu-id="453fa-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="453fa-139">Remarks</span></span>

<span data-ttu-id="453fa-140">Cuando se especifica un nombre de usuario o una contraseña incorrectos en el comando **wecutil SS** , no se genera ningún error hasta que se ve el estado de tiempo de ejecución de la suscripción mediante el comando **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="453fa-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="453fa-141">Establecer parámetros de configuración</span><span class="sxs-lookup"><span data-stu-id="453fa-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-143">Cadena que identifica de forma única una suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="453fa-144">Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG \_ archivo***</span><span class="sxs-lookup"><span data-stu-id="453fa-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-146">Valor que especifica la ruta de acceso al archivo XML que contiene la información de configuración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="453fa-147">La ruta de acceso puede ser absoluta o relativa al directorio actual.</span><span class="sxs-lookup"><span data-stu-id="453fa-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="453fa-148">Este parámetro solo se puede usar con los parámetros opcionales/CUS y/Cup y es mutuamente excluyente con todos los demás parámetros.</span><span class="sxs-lookup"><span data-stu-id="453fa-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *valor***</span><span class="sxs-lookup"><span data-stu-id="453fa-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-150">Valor que determina si se va a habilitar o deshabilitar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="453fa-151">El valor puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="453fa-151">VALUE can be true or false.</span></span> <span data-ttu-id="453fa-152">El valor predeterminado es true, que habilita la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-153">Cuando se deshabilita una suscripción iniciada por el recopilador, el origen del evento pasa a estar inactivo en lugar de deshabilitarse.</span><span class="sxs-lookup"><span data-stu-id="453fa-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="453fa-154">En una suscripción iniciada por el recopilador, puede deshabilitar un origen de eventos independiente de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Descripción***</span><span class="sxs-lookup"><span data-stu-id="453fa-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-156">Valor que especifica una descripción para la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *fecha y \_ hora***</span><span class="sxs-lookup"><span data-stu-id="453fa-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-158">Valor que especifica la hora de expiración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="453fa-159">*Fecha \_ TIME* es un valor especificado en el formato de fecha y hora XML estándar o ISO8601: "aaaa-mm-ddThh: mm: SS \[ . SSS \] \[ Z \] ", donde "T" es el separador de hora y "Z" indica la hora UTC.</span><span class="sxs-lookup"><span data-stu-id="453fa-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="453fa-160">Por ejemplo, si *fecha y \_ hora* es "2007-01-12T01:20:00", la hora de expiración de la suscripción es el 12 de enero de 2007 y 01:20.</span><span class="sxs-lookup"><span data-stu-id="453fa-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/Uri: *URI***</span><span class="sxs-lookup"><span data-stu-id="453fa-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-162">Valor que especifica el tipo de eventos utilizados por la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="453fa-163">La dirección del equipo de origen del evento junto con el identificador uniforme de recursos (URI) identifica de forma única el origen de los eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="453fa-164">La cadena URI se usa para todas las direcciones de origen de eventos de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *\_ modo de configuración***</span><span class="sxs-lookup"><span data-stu-id="453fa-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-166">Valor que especifica el modo de configuración de la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="453fa-167">*Configuración \_ de El modo* puede ser una de las cadenas siguientes: "normal", "Custom", "MinLatency" o "MinBandwidth".</span><span class="sxs-lookup"><span data-stu-id="453fa-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="453fa-168">La enumeración de modo de configuración de suscripción de EC define los modos de configuración. [**\_ \_ \_**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)</span><span class="sxs-lookup"><span data-stu-id="453fa-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="453fa-169">Los parámetros/DM,/DMI,/HI y/dmlt solo se pueden especificar si el modo de configuración está establecido en Custom.</span><span class="sxs-lookup"><span data-stu-id="453fa-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *consulta***</span><span class="sxs-lookup"><span data-stu-id="453fa-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-171">Valor que especifica la cadena de consulta de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="453fa-172">El formato de esta cadena puede ser diferente para los distintos valores de URI y se aplica a todos los orígenes de eventos de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/DIA: *dialecto***</span><span class="sxs-lookup"><span data-stu-id="453fa-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-174">Valor que especifica el dialecto que usa la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="453fa-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *formato***</span><span class="sxs-lookup"><span data-stu-id="453fa-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-176">Valor que especifica el formato de los eventos devueltos.</span><span class="sxs-lookup"><span data-stu-id="453fa-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="453fa-177">El *formato* puede ser "Events" o "RenderedText".</span><span class="sxs-lookup"><span data-stu-id="453fa-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="453fa-178">Cuando el valor es "RenderedText", los eventos se devuelven con las cadenas localizadas (por ejemplo, cadenas de descripción de eventos) adjuntas a los eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="453fa-179">El valor predeterminado de *Format* es "RenderedText".</span><span class="sxs-lookup"><span data-stu-id="453fa-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="453fa-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *configuración regional***</span><span class="sxs-lookup"><span data-stu-id="453fa-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-181">Valor que especifica la configuración regional para la entrega de las cadenas localizadas en formato de texto representado.</span><span class="sxs-lookup"><span data-stu-id="453fa-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="453fa-182">La *configuración regional* es un identificador de referencia cultural de idioma o país, por ejemplo, "en-US".</span><span class="sxs-lookup"><span data-stu-id="453fa-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="453fa-183">Este parámetro solo es válido cuando el parámetro/CF se establece en "RenderedText".</span><span class="sxs-lookup"><span data-stu-id="453fa-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="453fa-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree: \[ *valor*\]**</span><span class="sxs-lookup"><span data-stu-id="453fa-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-185">Valor que especifica los eventos que se van a entregar para la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="453fa-186">El *valor* puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="453fa-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="453fa-187">Cuando el *valor* es true, todos los eventos existentes se leen de los orígenes de eventos de suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="453fa-188">Cuando el *valor* es false, solo se entregan los eventos futuros (llegados).</span><span class="sxs-lookup"><span data-stu-id="453fa-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="453fa-189">El valor predeterminado es true cuando se especifica/REE sin un valor, y el valor predeterminado es false si no se especifica/REE.</span><span class="sxs-lookup"><span data-stu-id="453fa-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *nombre de archivo***</span><span class="sxs-lookup"><span data-stu-id="453fa-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-191">Valor que especifica el registro de eventos local que se usa para almacenar los eventos recibidos de la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *publicador***</span><span class="sxs-lookup"><span data-stu-id="453fa-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-193">Valor que especifica el nombre del publicador de eventos (proveedor).</span><span class="sxs-lookup"><span data-stu-id="453fa-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="453fa-194">Debe ser un publicador que posea o importe el registro especificado por el parámetro/LF.</span><span class="sxs-lookup"><span data-stu-id="453fa-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *modo***</span><span class="sxs-lookup"><span data-stu-id="453fa-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-196">Valor que especifica el modo de entrega de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="453fa-197">El *modo* puede ser de inserción o de extracción.</span><span class="sxs-lookup"><span data-stu-id="453fa-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="453fa-198">Esta opción solo es válida si el parámetro/cm está establecido en Custom.</span><span class="sxs-lookup"><span data-stu-id="453fa-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *número***</span><span class="sxs-lookup"><span data-stu-id="453fa-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-200">Valor que especifica el número máximo de elementos para la entrega por lotes en la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="453fa-201">Esta opción solo es válida si el parámetro/cm está establecido en Custom.</span><span class="sxs-lookup"><span data-stu-id="453fa-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span><span class="sxs-lookup"><span data-stu-id="453fa-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-203">Valor que especifica la latencia máxima permitida para entregar un lote de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="453fa-204">MS es el número de milisegundos permitidos.</span><span class="sxs-lookup"><span data-stu-id="453fa-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="453fa-205">Este parámetro solo es válido si el parámetro/cm está establecido en Custom.</span><span class="sxs-lookup"><span data-stu-id="453fa-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/HI: *MS***</span><span class="sxs-lookup"><span data-stu-id="453fa-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-207">Valor que especifica el intervalo de latido de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="453fa-208">*MS* es el número de milisegundos usados en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="453fa-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="453fa-209">Este parámetro solo es válido si el parámetro/cm está establecido en Custom.</span><span class="sxs-lookup"><span data-stu-id="453fa-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *nombredetransportedered***</span><span class="sxs-lookup"><span data-stu-id="453fa-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-211">Valor que especifica el nombre del transporte utilizado para conectarse al equipo de origen de eventos remotos.</span><span class="sxs-lookup"><span data-stu-id="453fa-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *\_ origen del evento***</span><span class="sxs-lookup"><span data-stu-id="453fa-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-213">Valor que especifica la dirección de un equipo de origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="453fa-214">*Evento \_ de ORIGEN* es una cadena que identifica un equipo de origen de eventos con el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="453fa-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="453fa-215">Este parámetro se puede utilizar con los parámetros/ese,/AES,/res o/un y/up.</span><span class="sxs-lookup"><span data-stu-id="453fa-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *valor***</span><span class="sxs-lookup"><span data-stu-id="453fa-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-217">Valor que determina si se va a habilitar o deshabilitar un origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="453fa-218">El *valor* puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="453fa-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="453fa-219">El valor predeterminado es true, que habilita el origen del evento.</span><span class="sxs-lookup"><span data-stu-id="453fa-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="453fa-220">Este parámetro solo se usa si se usa el parámetro/esa.</span><span class="sxs-lookup"><span data-stu-id="453fa-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span><span class="sxs-lookup"><span data-stu-id="453fa-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-222">Valor que agrega el origen de eventos especificado por el parámetro/esa si el origen del evento aún no forma parte de la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="453fa-223">Si el equipo especificado por el parámetro/esa ya forma parte de la suscripción, se muestra un error.</span><span class="sxs-lookup"><span data-stu-id="453fa-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="453fa-224">Este parámetro solo se permite si se usa el parámetro/esa.</span><span class="sxs-lookup"><span data-stu-id="453fa-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-225"><span id="_res"></span><span id="_RES"></span>**/res**</span><span class="sxs-lookup"><span data-stu-id="453fa-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-226">Valor que quita el origen de eventos especificado por el parámetro/esa si el origen del evento ya forma parte de la suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="453fa-227">Si el equipo especificado por el parámetro/esa no forma parte de la suscripción, se muestra un error.</span><span class="sxs-lookup"><span data-stu-id="453fa-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="453fa-228">Este parámetro solo se permite si se usa el parámetro/esa.</span><span class="sxs-lookup"><span data-stu-id="453fa-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *nombre de usuario***</span><span class="sxs-lookup"><span data-stu-id="453fa-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-230">Valor que especifica el nombre de usuario usado en las credenciales para conectarse al origen de eventos especificado en el parámetro/esa.</span><span class="sxs-lookup"><span data-stu-id="453fa-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="453fa-231">Este parámetro solo se permite si se usa el parámetro/esa.</span><span class="sxs-lookup"><span data-stu-id="453fa-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *contraseña***</span><span class="sxs-lookup"><span data-stu-id="453fa-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-233">Valor que especifica la contraseña para el nombre de usuario especificado en el parámetro/un.</span><span class="sxs-lookup"><span data-stu-id="453fa-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="453fa-234">Las credenciales de nombre de usuario y contraseña se usan para conectarse al origen de eventos especificado en el parámetro/esa.</span><span class="sxs-lookup"><span data-stu-id="453fa-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="453fa-235">Este parámetro solo se permite si se usa el parámetro/un.</span><span class="sxs-lookup"><span data-stu-id="453fa-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *TRANSPORTPORT***</span><span class="sxs-lookup"><span data-stu-id="453fa-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-237">Valor que especifica el número de puerto utilizado por el transporte al conectarse a un equipo de origen de eventos remoto.</span><span class="sxs-lookup"><span data-stu-id="453fa-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *nombre***</span><span class="sxs-lookup"><span data-stu-id="453fa-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-239">Valor que especifica el nombre DNS del equipo local.</span><span class="sxs-lookup"><span data-stu-id="453fa-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="453fa-240">Los orígenes de eventos remotos usan este nombre para volver a enviar eventos y deben usarse solo para suscripciones de extracción.</span><span class="sxs-lookup"><span data-stu-id="453fa-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *tipo***</span><span class="sxs-lookup"><span data-stu-id="453fa-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-242">Valor que especifica el tipo de credencial utilizado para tener acceso a los orígenes de eventos remotos.</span><span class="sxs-lookup"><span data-stu-id="453fa-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="453fa-243">El *tipo* puede ser "default", "Negotiate", "Digest", "Basic" o "LocalMachine".</span><span class="sxs-lookup"><span data-stu-id="453fa-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="453fa-244">El valor predeterminado es "default".</span><span class="sxs-lookup"><span data-stu-id="453fa-244">The default is "default".</span></span> <span data-ttu-id="453fa-245">Estos valores se definen en la enumeración de [**\_ \_ \_ tipo de credenciales de suscripción de EC**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) .</span><span class="sxs-lookup"><span data-stu-id="453fa-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nombre de usuario***</span><span class="sxs-lookup"><span data-stu-id="453fa-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-247">Valor que establece las credenciales de usuario compartidas que se usan para los orígenes de eventos que no tienen sus propias credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="453fa-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-248">Si este parámetro se usa con la opción/c, se omite la configuración de nombre de usuario y contraseña para los orígenes de eventos individuales del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="453fa-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="453fa-249">Si desea usar credenciales diferentes para un origen de eventos específico, puede invalidar este valor especificando los parámetros/un y/up para un origen de eventos específico en la línea de comandos de otro comando set-subscription.</span><span class="sxs-lookup"><span data-stu-id="453fa-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *contraseña***</span><span class="sxs-lookup"><span data-stu-id="453fa-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-251">Valor que establece la contraseña de usuario para las credenciales de usuario compartidas.</span><span class="sxs-lookup"><span data-stu-id="453fa-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="453fa-252">Cuando *contraseña* está establecida en \* (asterisco), la contraseña se lee desde la consola.</span><span class="sxs-lookup"><span data-stu-id="453fa-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="453fa-253">Esta opción solo es válida cuando se especifica el parámetro/cun.</span><span class="sxs-lookup"><span data-stu-id="453fa-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: *huellas digitales***</span><span class="sxs-lookup"><span data-stu-id="453fa-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-255">Valor que establece la lista de impresiones en miniatura del certificado del emisor, en una lista separada por comas.</span><span class="sxs-lookup"><span data-stu-id="453fa-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-256">Esta opción es específica solo para las suscripciones iniciadas por el origen.</span><span class="sxs-lookup"><span data-stu-id="453fa-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *permitido***</span><span class="sxs-lookup"><span data-stu-id="453fa-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-258">Valor que establece una lista separada por comas de cadena que especifica los nombres DNS de los equipos que no son de dominio y que pueden iniciar suscripciones.</span><span class="sxs-lookup"><span data-stu-id="453fa-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="453fa-259">Los nombres se pueden especificar mediante caracteres comodín, como " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="453fa-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="453fa-260">Esta lista aparece vacía de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="453fa-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-261">Esta opción es específica solo para las suscripciones iniciadas por el origen.</span><span class="sxs-lookup"><span data-stu-id="453fa-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *denegado***</span><span class="sxs-lookup"><span data-stu-id="453fa-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-263">Valor que establece una lista separada por comas de cadena que especifica los nombres DNS de los equipos que no son de dominio y a los que no se les permite iniciar suscripciones.</span><span class="sxs-lookup"><span data-stu-id="453fa-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="453fa-264">Los nombres se pueden especificar mediante caracteres comodín, como " \* . mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="453fa-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="453fa-265">Esta lista aparece vacía de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="453fa-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-266">Esta opción es específica solo para las suscripciones iniciadas por el origen.</span><span class="sxs-lookup"><span data-stu-id="453fa-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***</span><span class="sxs-lookup"><span data-stu-id="453fa-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-268">Valor que establece una cadena, en formato SDDL, que especifica qué equipos del dominio están permitidos o no para iniciar suscripciones.</span><span class="sxs-lookup"><span data-stu-id="453fa-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="453fa-269">El valor predeterminado es permitir que todos los equipos del dominio inicien las suscripciones.</span><span class="sxs-lookup"><span data-stu-id="453fa-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-270">Esta opción es específica solo para las suscripciones iniciadas por el origen.</span><span class="sxs-lookup"><span data-stu-id="453fa-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="453fa-271">Crear una suscripción</span><span class="sxs-lookup"><span data-stu-id="453fa-271">Create a New Subscription</span></span>

<span data-ttu-id="453fa-272">La siguiente sintaxis se usa para crear una suscripción de eventos para eventos en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="453fa-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="453fa-273">Observaciones</span><span class="sxs-lookup"><span data-stu-id="453fa-273">Remarks</span></span>

<span data-ttu-id="453fa-274">Cuando se especifica un nombre de usuario o una contraseña incorrectos en el comando **wecutil CS** , no se genera ningún error hasta que se ve el estado de tiempo de ejecución de la suscripción mediante el comando **wecutil gr** .</span><span class="sxs-lookup"><span data-stu-id="453fa-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="453fa-275">Parámetros de creación</span><span class="sxs-lookup"><span data-stu-id="453fa-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**archivo de configuración \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-277">Valor que especifica la ruta de acceso al archivo XML que contiene la información de configuración de la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="453fa-278">La ruta de acceso puede ser absoluta o relativa al directorio actual.</span><span class="sxs-lookup"><span data-stu-id="453fa-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="453fa-279">El siguiente código XML es un ejemplo de un archivo de configuración de suscripción que crea una suscripción iniciada por el recopilador para reenviar eventos del registro de eventos de aplicación de un equipo remoto al registro Eventos reenviados.</span><span class="sxs-lookup"><span data-stu-id="453fa-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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



<span data-ttu-id="453fa-280">El siguiente código XML es un ejemplo de un archivo de configuración de suscripción que crea una suscripción iniciada por el origen para reenviar eventos del registro de eventos de aplicación de un equipo remoto al registro Eventos reenviados.</span><span class="sxs-lookup"><span data-stu-id="453fa-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


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
> <span data-ttu-id="453fa-281">Al crear una suscripción iniciada por el origen, si **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers** / **IssuerCAList**, **AllowedSubjectList** y **DeniedSubjectList** están todos vacíos, se proporcionará un valor predeterminado para **AllowedSourceDomainComputers** -"O:NSG: NSD: (a;; GA;;;D C) (A;; GA;;; NS) ".</span><span class="sxs-lookup"><span data-stu-id="453fa-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="453fa-282">Este valor predeterminado de SDDL concede a los miembros del grupo de dominio equipos del dominio, así como al grupo servicio de red local (para el reenviador local), la capacidad de generar eventos para esta suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *nombre de usuario***</span><span class="sxs-lookup"><span data-stu-id="453fa-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-284">Valor que establece las credenciales de usuario compartidas que se usan para los orígenes de eventos que no tienen sus propias credenciales de usuario.</span><span class="sxs-lookup"><span data-stu-id="453fa-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="453fa-285">Este valor solo se aplica a las suscripciones iniciadas por el recopilador.</span><span class="sxs-lookup"><span data-stu-id="453fa-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="453fa-286">Si se especifica este parámetro, se omite la configuración de nombre de usuario y contraseña para los orígenes de eventos individuales del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="453fa-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="453fa-287">Si desea usar credenciales diferentes para un origen de eventos específico, puede invalidar este valor especificando los parámetros/un y/up para un origen de eventos específico en la línea de comandos de otro comando set-subscription.</span><span class="sxs-lookup"><span data-stu-id="453fa-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="453fa-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *contraseña***</span><span class="sxs-lookup"><span data-stu-id="453fa-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-289">Valor que establece la contraseña de usuario para las credenciales de usuario compartidas.</span><span class="sxs-lookup"><span data-stu-id="453fa-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="453fa-290">Cuando *password* se establece en " \* " (asterisco), la contraseña se lee desde la consola.</span><span class="sxs-lookup"><span data-stu-id="453fa-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="453fa-291">Esta opción solo es válida cuando se especifica el parámetro/cun.</span><span class="sxs-lookup"><span data-stu-id="453fa-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="453fa-292">Eliminar una suscripción</span><span class="sxs-lookup"><span data-stu-id="453fa-292">Delete a Subscription</span></span>

<span data-ttu-id="453fa-293">La siguiente sintaxis se usa para eliminar una suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="453fa-294">Parámetros de eliminación</span><span class="sxs-lookup"><span data-stu-id="453fa-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-296">Cadena que identifica de forma única una suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="453fa-297">Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="453fa-298">Se eliminará la suscripción identificada en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="453fa-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="453fa-299">Reintentar una suscripción</span><span class="sxs-lookup"><span data-stu-id="453fa-299">Retry a subscription</span></span>

<span data-ttu-id="453fa-300">La sintaxis siguiente se usa para reintentar una suscripción inactiva intentando reactivar todos los orígenes de eventos o especificados estableciendo una conexión a cada origen de eventos y enviando una solicitud de suscripción remota al origen de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="453fa-301">Los orígenes de eventos deshabilitados no se reintentan.</span><span class="sxs-lookup"><span data-stu-id="453fa-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="453fa-302">Parámetros de reintento</span><span class="sxs-lookup"><span data-stu-id="453fa-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**identificador de suscripción \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-304">Cadena que identifica de forma única una suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="453fa-305">Este identificador se especifica en el elemento **SubscriptionId** del archivo de configuración XML que se usa para crear la suscripción.</span><span class="sxs-lookup"><span data-stu-id="453fa-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="453fa-306">Se volverá a intentar la suscripción identificada en este parámetro.</span><span class="sxs-lookup"><span data-stu-id="453fa-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="453fa-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**origen del evento \_**</span><span class="sxs-lookup"><span data-stu-id="453fa-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="453fa-308">Valor que identifica un equipo que es un origen de eventos para una suscripción de eventos.</span><span class="sxs-lookup"><span data-stu-id="453fa-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="453fa-309">Este valor puede ser el nombre de dominio completo del equipo, el nombre NetBIOS o la dirección IP.</span><span class="sxs-lookup"><span data-stu-id="453fa-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="453fa-310">Configurar el servicio Recopilador de eventos de Windows</span><span class="sxs-lookup"><span data-stu-id="453fa-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="453fa-311">La siguiente sintaxis se utiliza para configurar el servicio Recopilador de eventos de Windows para garantizar que las suscripciones de eventos se puedan crear y mantener a través de reinicios del equipo.</span><span class="sxs-lookup"><span data-stu-id="453fa-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="453fa-312">Esto incluye el siguiente procedimiento:</span><span class="sxs-lookup"><span data-stu-id="453fa-312">This includes the following procedure:</span></span>

<span data-ttu-id="453fa-313">**Para configurar el servicio Recopilador de eventos de Windows**</span><span class="sxs-lookup"><span data-stu-id="453fa-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="453fa-314">Habilite el canal de eventos reenviados si está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="453fa-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="453fa-315">Retrasar el inicio del servicio Recopilador de eventos de Windows.</span><span class="sxs-lookup"><span data-stu-id="453fa-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="453fa-316">Inicie el servicio Recopilador de eventos de Windows si no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="453fa-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="453fa-317">Configurar parámetros del recopilador de eventos</span><span class="sxs-lookup"><span data-stu-id="453fa-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453fa-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *valor***</span><span class="sxs-lookup"><span data-stu-id="453fa-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="453fa-319">Un valor que determina si el comando de configuración rápida solicitará confirmación.</span><span class="sxs-lookup"><span data-stu-id="453fa-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="453fa-320">El valor puede ser true o false.</span><span class="sxs-lookup"><span data-stu-id="453fa-320">VALUE can be true or false.</span></span> <span data-ttu-id="453fa-321">Si el valor es true, el comando solicitará confirmación.</span><span class="sxs-lookup"><span data-stu-id="453fa-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="453fa-322">El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="453fa-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="453fa-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="453fa-323">Requirements</span></span>



| <span data-ttu-id="453fa-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="453fa-324">Requirement</span></span> | <span data-ttu-id="453fa-325">Value</span><span class="sxs-lookup"><span data-stu-id="453fa-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="453fa-326">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="453fa-326">Minimum supported client</span></span><br/> | <span data-ttu-id="453fa-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="453fa-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="453fa-328">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="453fa-328">Minimum supported server</span></span><br/> | <span data-ttu-id="453fa-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="453fa-329">Windows Server 2008</span></span><br/> |



 

 





