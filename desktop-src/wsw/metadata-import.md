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
# <a name="metadata-import"></a>Importación de metadatos

WWSAPI incluye elementos de API que se pueden usar para procesar el WSDL y la Directiva de un punto de conexión con el objetivo de extraer información que se puede usar para comunicarse con el punto de conexión. Estas API se suelen usar cuando el protocolo de comunicación compatible con el punto de conexión todavía no se conoce.


Use la siguiente secuencia para procesar los metadatos:

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

para obtener información sobre cómo se corresponden las aserciones de WSDL y WS-Policy con la API, vea el tema sobre la [asignación de metadatos](metadata-mapping.md) .

## <a name="security"></a>Seguridad

Los metadatos descargados son tan buenos como la dirección que se usa para descargarlos. Una aplicación debe asegurarse de que confía en la dirección. Además, una aplicación debe asegurarse de que utiliza un protocolo de seguridad para descargar los documentos de metadatos que no permiten la alteración de los metadatos.

Una aplicación debe inspeccionar las direcciones de los servicios expuestos por los metadatos. De forma predeterminada, el tiempo de ejecución garantiza que el nombre de host del servicio coincida con el de la dirección URL original utilizada para descargar los metadatos, pero es posible que la aplicación desee realizar comprobaciones adicionales. Una aplicación puede deshabilitar la comprobación del nombre de host mediante la sobrescritura de la [**\_ propiedad WS Metadata \_ Property \_ comprobar \_ \_ los nombres de host**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) . Si la comprobación del nombre de host que se realiza de forma predeterminada está deshabilitada, la aplicación tendrá que protegerse a través de los documentos de metadatos que contienen la dirección de un servicio de una entidad distinta de la que no confía de otra manera.

De forma predeterminada, la cantidad de memoria máxima utilizada por el tiempo de ejecución de metadatos para deserializar y procesar los metadatos es de 256 k y el número máximo de documentos que se pueden agregar es 32. Estos valores predeterminados se pueden sobrescribir con el montón de propiedades de [**\_ metadatos de WS \_ \_ \_ \_ tamaño solicitado**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) y propiedades de **\_ metadatos \_ \_ \_ de WS** . Estos límites están diseñados para limitar la cantidad de descargas y limitar la cantidad de memoria asignada para acumular los metadatos. Si se aumentan estos valores, puede producirse un uso excesivo de la memoria, el uso de la CPU o el consumo de ancho de banda de red. Tenga en cuenta que, debido a la expansión de cadenas de diccionario en el formato binario, un mensaje pequeño puede conducir a una forma deserializada mucho más grande, por lo que confiar en pequeños mensajes para limitar la asignación de memoria de los metadatos no es suficiente cuando se usa el formato binario.

De forma predeterminada, el número máximo de alternativas de directiva es 32, aunque se puede sobrescribir mediante la propiedad de la [**propiedad de directiva de WS \_ \_ \_ Max \_ Alternatives**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) . Si una aplicación recorre en bucle cada alternativa buscando una coincidencia, puede que tenga que buscar todas las alternativas antes de encontrar una coincidencia. Aumentar el número máximo de alternativas puede dar lugar a un uso excesivo de la CPU.

Las enumeraciones siguientes forman parte de la importación de metadatos:

-   [**\_identificador de propiedad de metadatos de WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**\_Estado de metadatos de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**\_tipo de \_ extensión de directiva de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**identificador de la propiedad de directiva de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**\_Estado de directiva de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**\_tipo de \_ restricción de enlace \_ \_ de WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

Las siguientes funciones forman parte de la importación de metadatos:

-   [**WsCreateMetadata**](/windows/desktop/api/WebServices/nf-webservices-wscreatemetadata)
-   [**WsFreeMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsfreemetadata)
-   [**WsGetMetadataEndpoints**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataendpoints)
-   [**WsGetMetadataProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetmetadataproperty)
-   [**WsGetMissingMetadataDocumentAddress**](/windows/desktop/api/WebServices/nf-webservices-wsgetmissingmetadatadocumentaddress)
-   [**WsGetPolicyAlternativeCount**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyalternativecount)
-   [**WsGetPolicyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetpolicyproperty)
-   [**WsMatchPolicyAlternative**](/windows/desktop/api/WebServices/nf-webservices-wsmatchpolicyalternative)
-   [**WsReadMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsreadmetadata)
-   [**WsResetMetadata**](/windows/desktop/api/WebServices/nf-webservices-wsresetmetadata)

Los siguientes identificadores forman parte de la importación de metadatos:

-   [metadatos de WS \_](ws-metadata.md)
-   [Directiva de WS \_](ws-policy.md)

Las siguientes estructuras forman parte de la importación de metadatos:

-   [**\_restricción de \_ enlace de seguridad de mensajes de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restricción de \_ propiedad de canal de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**extensión de directiva de punto de conexión de WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**\_restricción de \_ \_ enlace de seguridad de autenticación de encabezado \_ http \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**\_restricción de \_ \_ enlace de seguridad de mensaje de token \_ emitido \_ de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**\_restricción de \_ \_ enlace de \_ seguridad de mensaje \_ \_ WS Kerberos APREQ**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_extremo de metadatos de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**\_extremos de metadatos de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**\_propiedad de metadatos de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**\_restricciones de directivas de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**\_extensión de directiva de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**propiedades de la Directiva de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**\_propiedad de directiva de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**\_restricción de \_ propiedad de token de seguridad de solicitud WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**restricción de enlace de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**\_restricción de \_ propiedad de enlace \_ \_ de WS Security**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**\_restricciones de seguridad de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**\_restricción de \_ \_ enlace de seguridad de mensaje de contexto \_ de \_ WS Security \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**restricción de propiedad de WS \_ Security \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**\_restricción de \_ \_ enlace de seguridad de transporte SSL \_ de \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**\_restricción de \_ \_ enlace de seguridad de transporte SSPI \_ \_ de WS TCP \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**\_restricción de \_ enlace de seguridad de mensaje \_ \_ de WS username \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




