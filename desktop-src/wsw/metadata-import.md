---
title: Importación de metadatos
description: WWSAPI incluye elementos de API que se pueden usar para procesar el WSDL y la Directiva de un punto de conexión con el objetivo de extraer información que se puede usar para comunicarse con el punto de conexión.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Servicios Web de importación de metadatos para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c36ffdf9bcbf0d63bdef473cc52cd4d545e5a3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797392"
---
# <a name="metadata-import"></a><span data-ttu-id="103b3-106">Importación de metadatos</span><span class="sxs-lookup"><span data-stu-id="103b3-106">Metadata Import</span></span>

<span data-ttu-id="103b3-107">WWSAPI incluye elementos de API que se pueden usar para procesar el WSDL y la Directiva de un punto de conexión con el objetivo de extraer información que se puede usar para comunicarse con el punto de conexión.</span><span class="sxs-lookup"><span data-stu-id="103b3-107">The WWSAPI includes API elements that can be used to process WSDL and Policy from an endpoint with the goal of extracting information that can be used to communicate with the endpoint.</span></span> <span data-ttu-id="103b3-108">Estas API se suelen usar cuando el protocolo de comunicación compatible con el punto de conexión todavía no se conoce.</span><span class="sxs-lookup"><span data-stu-id="103b3-108">These APIs are typically used when the communication protocol supported by the endpoint is not already known.</span></span>


<span data-ttu-id="103b3-109">Use la siguiente secuencia para procesar los metadatos:</span><span class="sxs-lookup"><span data-stu-id="103b3-109">Use the following sequence to process metadata:</span></span>

``` syntax
WsCreateMetadata    // create a metadata object

while there are metadata documents to add
{
    // retrieve the metadata document from it's location
    // (download, read from file, etc)

    // add the document to the metadata object
    WsReadMetadata

    // optionally query the metadata object for any missing documents
    WsGetMissingMetadataDocumentAddress?
}

// get the endpoints from the metadata object
WsGetMetadataEndpoints

for each endpoint
{            
    // examine the endpoint information to see if 
    // the endpoint is relevant for the particular scenario

    if the endpoint is relevant
    {
        // get the policy object from the endpoint

        // get the number of policy alternatives in the policy
        WsGetPolicyAlternativeCount

        for each policy alternative
        {
            // construct a policy constraints structure that specifies
            // what policy is acceptable and what information to extract
            // from the policy

            // see if the policy alternative matches the constraints
            WsMatchPolicyAlternative

            // if there is a match, then use it

            // if there is not a match, then it is also possible to 
            // try with a different constraint structure
        }
    }
}

// If reusing the metadata object for a different set of documents
WsResetMetadata? // reset metadata object, which removes all documents

WsFreeMetadata // free the metadata object
```

<span data-ttu-id="103b3-110">para obtener información sobre cómo se corresponden las aserciones de WSDL y WS-Policy con la API, vea el tema sobre la [asignación de metadatos](metadata-mapping.md) .</span><span class="sxs-lookup"><span data-stu-id="103b3-110">for information about how WSDL and WS-Policy assertions correspond to the API, see the [Metadata Mapping](metadata-mapping.md) topic.</span></span>

## <a name="security"></a><span data-ttu-id="103b3-111">Seguridad</span><span class="sxs-lookup"><span data-stu-id="103b3-111">Security</span></span>

<span data-ttu-id="103b3-112">Los metadatos descargados son tan buenos como la dirección que se usa para descargarlos.</span><span class="sxs-lookup"><span data-stu-id="103b3-112">The metadata downloaded is only as good as the address used to download it.</span></span> <span data-ttu-id="103b3-113">Una aplicación debe asegurarse de que confía en la dirección.</span><span class="sxs-lookup"><span data-stu-id="103b3-113">An application should ensure that is trusts the address.</span></span> <span data-ttu-id="103b3-114">Además, una aplicación debe asegurarse de que utiliza un protocolo de seguridad para descargar los documentos de metadatos que no permiten la alteración de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="103b3-114">Also, an application should ensure that it uses a security protocol to download the metadata documents that does not allow tampering with the metadata.</span></span>

<span data-ttu-id="103b3-115">Una aplicación debe inspeccionar las direcciones de los servicios expuestos por los metadatos.</span><span class="sxs-lookup"><span data-stu-id="103b3-115">An application should inspect the addresses of the services exposed by the metadata.</span></span> <span data-ttu-id="103b3-116">De forma predeterminada, el tiempo de ejecución garantiza que el nombre de host del servicio coincida con el de la dirección URL original utilizada para descargar los metadatos, pero es posible que la aplicación desee realizar comprobaciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="103b3-116">By default, the runtime ensures that the host name of the service matches that of the original URL used to download the metadata, but the application may want to perform additional checks.</span></span> <span data-ttu-id="103b3-117">Una aplicación puede deshabilitar la comprobación del nombre de host mediante la sobrescritura de la [**\_ propiedad WS Metadata \_ Property \_ comprobar \_ \_ los nombres de host**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) .</span><span class="sxs-lookup"><span data-stu-id="103b3-117">An application can disable the host name verification by overwriting [**WS\_METADATA\_PROPERTY\_VERIFY\_HOST\_NAMES**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) property.</span></span> <span data-ttu-id="103b3-118">Si la comprobación del nombre de host que se realiza de forma predeterminada está deshabilitada, la aplicación tendrá que protegerse a través de los documentos de metadatos que contienen la dirección de un servicio de una entidad distinta de la que no confía de otra manera.</span><span class="sxs-lookup"><span data-stu-id="103b3-118">If the hostname check that is done by default is disabled, the application will need to protect itself against the metadata documents containing the address of a service from a different party that it does not trust in some other way.</span></span>

<span data-ttu-id="103b3-119">De forma predeterminada, la cantidad de memoria máxima utilizada por el tiempo de ejecución de metadatos para deserializar y procesar los metadatos es de 256 k y el número máximo de documentos que se pueden agregar es 32.</span><span class="sxs-lookup"><span data-stu-id="103b3-119">By default, the maximum amount of memory used by the metadata runtime to deserialize and process the metadata is 256k, and the maximum number of documents that may be added is 32.</span></span> <span data-ttu-id="103b3-120">Estos valores predeterminados se pueden sobrescribir con el montón de propiedades de [**\_ metadatos de WS \_ \_ \_ \_ tamaño solicitado**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) y propiedades de **\_ metadatos \_ \_ \_ de WS** .</span><span class="sxs-lookup"><span data-stu-id="103b3-120">These default values can be overwritten by [**WS\_METADATA\_PROPERTY\_HEAP\_REQUESTED\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) and **WS\_METADATA\_PROPERTY\_MAX\_DOCUMENTS** properties.</span></span> <span data-ttu-id="103b3-121">Estos límites están diseñados para limitar la cantidad de descargas y limitar la cantidad de memoria asignada para acumular los metadatos.</span><span class="sxs-lookup"><span data-stu-id="103b3-121">These bounds are designed to limit the amount of downloads and limit the amount of memory allocated in order to accumulate the metadata.</span></span> <span data-ttu-id="103b3-122">Si se aumentan estos valores, puede producirse un uso excesivo de la memoria, el uso de la CPU o el consumo de ancho de banda de red.</span><span class="sxs-lookup"><span data-stu-id="103b3-122">Increasing these values may lead to excessive memory usage, CPU usage, or network bandwidth consumption.</span></span> <span data-ttu-id="103b3-123">Tenga en cuenta que, debido a la expansión de cadenas de diccionario en el formato binario, un mensaje pequeño puede conducir a una forma deserializada mucho más grande, por lo que confiar en pequeños mensajes para limitar la asignación de memoria de los metadatos no es suficiente cuando se usa el formato binario.</span><span class="sxs-lookup"><span data-stu-id="103b3-123">Note that due to expansion of dictionary strings in the binary format, a small message may lead to a much larger deserialized form, so relying on small messages to limit metadata memory allocation is not sufficient when using the binary format.</span></span>

<span data-ttu-id="103b3-124">De forma predeterminada, el número máximo de alternativas de directiva es 32, aunque se puede sobrescribir mediante la propiedad de la [**propiedad de directiva de WS \_ \_ \_ Max \_ Alternatives**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) .</span><span class="sxs-lookup"><span data-stu-id="103b3-124">By default, the maximum number of policy alternatives is 32, though it can be overwritten by [**WS\_POLICY\_PROPERTY\_MAX\_ALTERNATIVES**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) property.</span></span> <span data-ttu-id="103b3-125">Si una aplicación recorre en bucle cada alternativa buscando una coincidencia, puede que tenga que buscar todas las alternativas antes de encontrar una coincidencia.</span><span class="sxs-lookup"><span data-stu-id="103b3-125">If an application loops through each alternative looking for a match, it may need to search all alternatives before finding a match.</span></span> <span data-ttu-id="103b3-126">Aumentar el número máximo de alternativas puede dar lugar a un uso excesivo de la CPU.</span><span class="sxs-lookup"><span data-stu-id="103b3-126">Increasing the maximum number of alternatives may lead to excessive CPU utilization.</span></span>

<span data-ttu-id="103b3-127">Las enumeraciones siguientes forman parte de la importación de metadatos:</span><span class="sxs-lookup"><span data-stu-id="103b3-127">The following enumerations are part of metadata import:</span></span>

-   [<span data-ttu-id="103b3-128">**\_identificador de propiedad de metadatos de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-128">**WS\_METADATA\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [<span data-ttu-id="103b3-129">**\_Estado de metadatos de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-129">**WS\_METADATA\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [<span data-ttu-id="103b3-130">**\_tipo de \_ extensión de directiva de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-130">**WS\_POLICY\_EXTENSION\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [<span data-ttu-id="103b3-131">**identificador de la propiedad de directiva de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-131">**WS\_POLICY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [<span data-ttu-id="103b3-132">**\_Estado de directiva de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-132">**WS\_POLICY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [<span data-ttu-id="103b3-133">**\_tipo de \_ restricción de enlace \_ \_ de WS Security**</span><span class="sxs-lookup"><span data-stu-id="103b3-133">**WS\_SECURITY\_BINDING\_CONSTRAINT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

<span data-ttu-id="103b3-134">Las siguientes funciones forman parte de la importación de metadatos:</span><span class="sxs-lookup"><span data-stu-id="103b3-134">The following functions are part of metadata import:</span></span>

-   [<span data-ttu-id="103b3-135">**WsCreateMetadata**</span><span class="sxs-lookup"><span data-stu-id="103b3-135">**WsCreateMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [<span data-ttu-id="103b3-136">**WsFreeMetadata**</span><span class="sxs-lookup"><span data-stu-id="103b3-136">**WsFreeMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [<span data-ttu-id="103b3-137">**WsGetMetadataEndpoints**</span><span class="sxs-lookup"><span data-stu-id="103b3-137">**WsGetMetadataEndpoints**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [<span data-ttu-id="103b3-138">**WsGetMetadataProperty**</span><span class="sxs-lookup"><span data-stu-id="103b3-138">**WsGetMetadataProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [<span data-ttu-id="103b3-139">**WsGetMissingMetadataDocumentAddress**</span><span class="sxs-lookup"><span data-stu-id="103b3-139">**WsGetMissingMetadataDocumentAddress**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [<span data-ttu-id="103b3-140">**WsGetPolicyAlternativeCount**</span><span class="sxs-lookup"><span data-stu-id="103b3-140">**WsGetPolicyAlternativeCount**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [<span data-ttu-id="103b3-141">**WsGetPolicyProperty**</span><span class="sxs-lookup"><span data-stu-id="103b3-141">**WsGetPolicyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [<span data-ttu-id="103b3-142">**WsMatchPolicyAlternative**</span><span class="sxs-lookup"><span data-stu-id="103b3-142">**WsMatchPolicyAlternative**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [<span data-ttu-id="103b3-143">**WsReadMetadata**</span><span class="sxs-lookup"><span data-stu-id="103b3-143">**WsReadMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [<span data-ttu-id="103b3-144">**WsResetMetadata**</span><span class="sxs-lookup"><span data-stu-id="103b3-144">**WsResetMetadata**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

<span data-ttu-id="103b3-145">Los siguientes identificadores forman parte de la importación de metadatos:</span><span class="sxs-lookup"><span data-stu-id="103b3-145">The following handles are part of metadata import:</span></span>

-   [<span data-ttu-id="103b3-146">metadatos de WS \_</span><span class="sxs-lookup"><span data-stu-id="103b3-146">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="103b3-147">Directiva de WS \_</span><span class="sxs-lookup"><span data-stu-id="103b3-147">WS\_POLICY</span></span>](ws-policy.md)

<span data-ttu-id="103b3-148">Las siguientes estructuras forman parte de la importación de metadatos:</span><span class="sxs-lookup"><span data-stu-id="103b3-148">The following structures are part of metadata import:</span></span>

-   [<span data-ttu-id="103b3-149">**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-149">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="103b3-150">**\_restricción de \_ propiedad de canal de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-150">**WS\_CHANNEL\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [<span data-ttu-id="103b3-151">**extensión de directiva de punto de conexión de WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-151">**WS\_ENDPOINT\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [<span data-ttu-id="103b3-152">**\_restricción de \_ \_ enlace de seguridad de autenticación de encabezado \_ http \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-152">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [<span data-ttu-id="103b3-153">**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-153">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [<span data-ttu-id="103b3-154">**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**</span><span class="sxs-lookup"><span data-stu-id="103b3-154">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="103b3-155">**\_extremo de metadatos de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-155">**WS\_METADATA\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [<span data-ttu-id="103b3-156">**\_extremos de metadatos de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-156">**WS\_METADATA\_ENDPOINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [<span data-ttu-id="103b3-157">**\_propiedad de metadatos de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-157">**WS\_METADATA\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [<span data-ttu-id="103b3-158">**\_restricciones de directivas de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-158">**WS\_POLICY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [<span data-ttu-id="103b3-159">**\_extensión de directiva de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-159">**WS\_POLICY\_EXTENSION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [<span data-ttu-id="103b3-160">**propiedades de la Directiva de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-160">**WS\_POLICY\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [<span data-ttu-id="103b3-161">**\_propiedad de directiva de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-161">**WS\_POLICY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [<span data-ttu-id="103b3-162">**\_restricción de \_ propiedad de token de seguridad de solicitud WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-162">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [<span data-ttu-id="103b3-163">**restricción de enlace de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-163">**WS\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [<span data-ttu-id="103b3-164">**\_restricción de \_ propiedad de enlace \_ \_ de WS Security**</span><span class="sxs-lookup"><span data-stu-id="103b3-164">**WS\_SECURITY\_BINDING\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [<span data-ttu-id="103b3-165">**\_restricciones de seguridad de WS \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-165">**WS\_SECURITY\_CONSTRAINTS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [<span data-ttu-id="103b3-166">**\_restricción de \_ \_ enlace de seguridad de mensaje de contexto \_ de \_ WS Security \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-166">**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [<span data-ttu-id="103b3-167">**restricción de propiedad de WS \_ Security \_ \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-167">**WS\_SECURITY\_PROPERTY\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [<span data-ttu-id="103b3-168">**\_restricción de \_ \_ enlace de seguridad de transporte SSL \_ de \_ WS**</span><span class="sxs-lookup"><span data-stu-id="103b3-168">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [<span data-ttu-id="103b3-169">**\_restricción de \_ \_ enlace de seguridad de transporte SSPI \_ \_ de WS TCP \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-169">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [<span data-ttu-id="103b3-170">**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**</span><span class="sxs-lookup"><span data-stu-id="103b3-170">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




