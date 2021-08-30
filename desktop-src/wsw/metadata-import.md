---
title: Importación de metadatos
description: WWSAPI incluye elementos de API que se pueden usar para procesar WSDL y Policy desde un punto de conexión con el objetivo de extraer información que se puede usar para comunicarse con el punto de conexión.
ms.assetid: 77738bf1-ef8b-4fd6-a36a-43f1932868dd
keywords:
- Servicios web de importación de metadatos para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8b213971a8d4e9872bde86f4ef9c7693eb104aa7289f5fdf3dbf32ce239ab0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089565"
---
# <a name="metadata-import"></a>Importación de metadatos

WWSAPI incluye elementos de API que se pueden usar para procesar WSDL y Policy desde un punto de conexión con el objetivo de extraer información que se puede usar para comunicarse con el punto de conexión. Estas API se usan normalmente cuando aún no se conoce el protocolo de comunicación compatible con el punto de conexión.


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

Para obtener información sobre cómo wsdl y WS-Policy aserciones corresponden a la API, vea el tema [Asignación de](metadata-mapping.md) metadatos.

## <a name="security"></a>Seguridad

Los metadatos descargados son tan buenos como la dirección usada para descargarlos. Una aplicación debe asegurarse de que confía en la dirección. Además, una aplicación debe asegurarse de que usa un protocolo de seguridad para descargar los documentos de metadatos que no permiten manipular los metadatos.

Una aplicación debe inspeccionar las direcciones de los servicios expuestos por los metadatos. De forma predeterminada, el tiempo de ejecución garantiza que el nombre de host del servicio coincide con el de la dirección URL original usada para descargar los metadatos, pero es posible que la aplicación quiera realizar comprobaciones adicionales. Una aplicación puede deshabilitar la comprobación del nombre de host sobrescribiendo la propiedad [**VERIFY HOST NAMES \_ \_ \_ \_ \_ de WS METADATA PROPERTY.**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) Si la comprobación de nombre de host que se realiza de forma predeterminada está deshabilitada, la aplicación tendrá que protegerse contra los documentos de metadatos que contienen la dirección de un servicio de otra parte en la que no confía de alguna otra manera.

De forma predeterminada, la cantidad máxima de memoria que usa el tiempo de ejecución de metadatos para deserializar y procesar los metadatos es de 256 000 y el número máximo de documentos que se pueden agregar es 32. Estos valores predeterminados se pueden sobrescribir mediante las propiedades [**WS \_ METADATA PROPERTY \_ \_ HEAP REQUESTED \_ \_ SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id) y **WS METADATA PROPERTY MAX \_ \_ \_ \_ DOCUMENTS.** Estos límites están diseñados para limitar la cantidad de descargas y limitar la cantidad de memoria asignada para acumular los metadatos. Aumentar estos valores puede provocar un uso excesivo de memoria, uso de CPU o consumo de ancho de banda de red. Tenga en cuenta que debido a la expansión de cadenas de diccionario en formato binario, un mensaje pequeño puede dar lugar a un formato deserializador mucho mayor, por lo que confiar en mensajes pequeños para limitar la asignación de memoria de metadatos no es suficiente cuando se usa el formato binario.

De forma predeterminada, el número máximo de alternativas de directiva es 32, aunque se puede sobrescribir mediante la propiedad [**\_ WS POLICY \_ PROPERTY MAX \_ \_ ALTERNATIVES.**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id) Si una aplicación recorre en bucle cada alternativa que busca una coincidencia, puede que tenga que buscar todas las alternativas antes de encontrar una coincidencia. Aumentar el número máximo de alternativas puede provocar un uso excesivo de la CPU.

Las enumeraciones siguientes forman parte de la importación de metadatos:

-   [**IDENTIFICADOR DE PROPIEDAD \_ DE METADATOS \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_property_id)
-   [**ESTADO DE METADATOS DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_metadata_state)
-   [**TIPO DE EXTENSIÓN \_ DE \_ DIRECTIVA DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_extension_type)
-   [**ID. \_ DE PROPIEDAD DE LA DIRECTIVA \_ DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_property_id)
-   [**ESTADO DE LA DIRECTIVA DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_policy_state)
-   [**TIPO DE \_ RESTRICCIÓN DE ENLACE DE SEGURIDAD \_ \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_constraint_type)

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

-   [METADATOS DE WS \_](ws-metadata.md)
-   [WS \_ POLICY](ws-policy.md)

Las estructuras siguientes forman parte de la importación de metadatos:

-   [**WS \_ CERT \_ MESSAGE \_ SECURITY \_ BINDING \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ PROPIEDAD \_ DEL CANAL WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property_constraint)
-   [**EXTENSIÓN DE DIRECTIVA \_ DE PUNTO DE CONEXIÓN \_ DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_policy_extension)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE \_ \_ AUTENTICACIÓN DE \_ ENCABEZADO \_ \_ HTTP WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE MENSAJES DE TOKEN \_ \_ \_ EMITIDOS \_ \_ POR WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)
-   [**WS \_ KERBEROS \_ APREQ \_ MESSAGE \_ SECURITY \_ BINDING \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**PUNTO DE CONEXIÓN DE METADATOS DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoint)
-   [**PUNTOS DE CONEXIÓN \_ DE \_ METADATOS DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_endpoints)
-   [**PROPIEDAD DE METADATOS DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_metadata_property)
-   [**RESTRICCIONES \_ DE DIRECTIVA DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_constraints)
-   [**EXTENSIÓN DE DIRECTIVA DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_extension)
-   [**PROPIEDADES DE LA DIRECTIVA DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_properties)
-   [**WS \_ POLICY \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_policy_property)
-   [**RESTRICCIÓN DE PROPIEDAD \_ DEL TOKEN DE SEGURIDAD DE \_ \_ \_ WS \_ REQUEST**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE \_ DE SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_constraint)
-   [**RESTRICCIÓN DE PROPIEDAD \_ \_ DE ENLACE DE \_ SEGURIDAD DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property_constraint)
-   [**RESTRICCIONES \_ DE SEGURIDAD DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_constraints)
-   [**RESTRICCIÓN DE ENLACE \_ DE SEGURIDAD DEL MENSAJE DE CONTEXTO DE \_ \_ \_ \_ \_ SEGURIDAD DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint)
-   [**RESTRICCIÓN DE \_ PROPIEDAD \_ DE SEGURIDAD DE WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property_constraint)
-   [**RESTRICCIÓN DE \_ ENLACE DE SEGURIDAD DE TRANSPORTE SSL DE WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)
-   [**RESTRICCIÓN DE ENLACE DE SEGURIDAD DE TRANSPORTE DE WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)
-   [**RESTRICCIÓN DE ENLACE \_ DE SEGURIDAD DE MENSAJES DE NOMBRE DE \_ \_ \_ USUARIO DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)

 

 




