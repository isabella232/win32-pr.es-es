---
title: Definir plantillas de datos de eventos
description: Los proveedores usan plantillas de datos para definir los datos específicos del evento que incluyen con un evento y para definir los datos de filtro que una sesión de seguimiento de ETW puede pasar al proveedor cuando habilita el proveedor.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "103904448"
---
# <a name="defining-event-data-templates"></a><span data-ttu-id="19c4f-103">Definir plantillas de datos de eventos</span><span class="sxs-lookup"><span data-stu-id="19c4f-103">Defining Event Data Templates</span></span>

<span data-ttu-id="19c4f-104">Los proveedores usan plantillas de datos para definir los datos específicos del evento que incluyen con un evento y para definir los datos de filtro que una sesión de seguimiento de ETW puede pasar al proveedor cuando habilita el proveedor.</span><span class="sxs-lookup"><span data-stu-id="19c4f-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="19c4f-105">Si el evento no incluye datos específicos del evento, no definirá una plantilla.</span><span class="sxs-lookup"><span data-stu-id="19c4f-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="19c4f-106">Para definir una plantilla, use el elemento de **plantilla** .</span><span class="sxs-lookup"><span data-stu-id="19c4f-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="19c4f-107">Una plantilla incluye un elemento de datos para cada fragmento de datos que el proveedor incluye con el evento.</span><span class="sxs-lookup"><span data-stu-id="19c4f-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="19c4f-108">Puede especificar tipos enteros, cadenas, matrices y estructuras.</span><span class="sxs-lookup"><span data-stu-id="19c4f-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="19c4f-109">Debe escribir los datos de evento en el orden en que se definieron los elementos de datos en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="19c4f-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="19c4f-110">También puede incluir en la plantilla, un fragmento XML que los consumidores deben usar para determinar cómo se representan los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="19c4f-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="19c4f-111">Si no incluye el fragmento, los consumidores deben representar los datos del evento en el orden en que se definieron los elementos de datos en la plantilla.</span><span class="sxs-lookup"><span data-stu-id="19c4f-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="19c4f-112">Al definir una plantilla, debe asignarle un identificador de plantilla que use para hacer referencia a la plantilla en una definición de evento.</span><span class="sxs-lookup"><span data-stu-id="19c4f-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="19c4f-113">Cada elemento de datos de la plantilla debe especificar un nombre y un tipo de datos de entrada (para obtener una lista de tipos de entrada, vea la sección Comentarios del tipo complejo [**InputType**](eventmanifestschema-inputtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="19c4f-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="19c4f-114">Si el tipo de datos de entrada se puede representar en varios formatos, debe especificar el tipo de datos de salida que indica a los consumidores cómo representar el elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="19c4f-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="19c4f-115">Por ejemplo, un tipo de datos de entrada UInt32 se puede representar como un entero sin signo, un identificador de subproceso, una dirección IPv4 y un código de error de Win32 entre otros.</span><span class="sxs-lookup"><span data-stu-id="19c4f-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="19c4f-116">Si no especifica el tipo de datos de salida, los consumidores deben usar el tipo de salida predeterminado del tipo de entrada para representar el elemento de datos.</span><span class="sxs-lookup"><span data-stu-id="19c4f-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="19c4f-117">Para especificar una matriz, incluya el atributo **Count** en el elemento de datos y establézcalo en el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="19c4f-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="19c4f-118">La matriz puede ser una matriz de tamaño variable o una matriz de tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="19c4f-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="19c4f-119">Si la matriz es una matriz de tamaño fijo, establezca **Count** en el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="19c4f-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="19c4f-120">Por ejemplo, si una matriz de enteros tiene un tamaño fijo de 10, establezca **Count** en 10.</span><span class="sxs-lookup"><span data-stu-id="19c4f-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="19c4f-121">Al escribir la matriz, debe escribir 40 bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="19c4f-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="19c4f-122">Si la matriz es una matriz de tamaño variable, establezca **Count** en el nombre del elemento de datos que contiene el tamaño de la matriz.</span><span class="sxs-lookup"><span data-stu-id="19c4f-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="19c4f-123">Si la matriz contiene punteros, la dirección de los punteros se escriben como los datos de evento, no los datos a los que apuntan los punteros.</span><span class="sxs-lookup"><span data-stu-id="19c4f-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="19c4f-124">Debe especificar el atributo de **longitud** si el elemento de datos es un BLOB binario.</span><span class="sxs-lookup"><span data-stu-id="19c4f-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="19c4f-125">También puede especificar el atributo de **longitud** para las cadenas de longitud fija.</span><span class="sxs-lookup"><span data-stu-id="19c4f-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="19c4f-126">Especifique el atributo **map** si el elemento de datos representa un valor de enumeración y desea que el consumidor imprima una cadena para el valor en lugar del propio valor.</span><span class="sxs-lookup"><span data-stu-id="19c4f-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="19c4f-127">Si incluye estructuras en la plantilla, debe escribir los miembros de la estructura individualmente en lugar de escribir la estructura a menos que pueda garantizar la alineación de los límites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="19c4f-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="19c4f-128">Debe considerar detenidamente la información que se incluye en los eventos, sobre todo cuando los eventos se escriben en los canales globales.</span><span class="sxs-lookup"><span data-stu-id="19c4f-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="19c4f-129">Como norma general, no debe incluir información privada en los eventos.</span><span class="sxs-lookup"><span data-stu-id="19c4f-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="19c4f-130">Esto incluye las contraseñas de texto no cifrado y la información personal del usuario.</span><span class="sxs-lookup"><span data-stu-id="19c4f-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="19c4f-131">Además, los programas que ejecuta el usuario, las direcciones URL que el usuario visitó y otra información relacionada con las actividades del usuario en el equipo deben considerarse privados.</span><span class="sxs-lookup"><span data-stu-id="19c4f-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="19c4f-132">Si debe registrar las direcciones URL y los nombres de usuario en los eventos, no los escriba en los canales de Windows (sistema y aplicación) porque todos los usuarios autenticados pueden leer estos canales.</span><span class="sxs-lookup"><span data-stu-id="19c4f-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="19c4f-133">En su lugar, escríbalos en sus propios canales operativos o analíticos.</span><span class="sxs-lookup"><span data-stu-id="19c4f-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="19c4f-134">Establezca los permisos de acceso en estos canales para permitir que solo los administradores lean los eventos.</span><span class="sxs-lookup"><span data-stu-id="19c4f-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="19c4f-135">Es posible que tenga que proporcionar una divulgación adecuada para notificar a los usuarios que la información privada está disponible para los administradores.</span><span class="sxs-lookup"><span data-stu-id="19c4f-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="19c4f-136">En el ejemplo siguiente se muestra cómo definir una plantilla.</span><span class="sxs-lookup"><span data-stu-id="19c4f-136">The following example shows how to define a template.</span></span> <span data-ttu-id="19c4f-137">Debe especificar el atributo **TID** de la plantilla al que hace referencia en la definición de evento o en la definición de filtro.</span><span class="sxs-lookup"><span data-stu-id="19c4f-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
