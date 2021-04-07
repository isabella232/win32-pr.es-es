---
title: Errors
description: En esta sección se describen los errores que pueden ser problemas de las funciones de servicios Web de Windows en el resultado de un error al ejecutar el comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Servicios Web de errores para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903251"
---
# <a name="errors"></a>Errors

En esta sección se describen los errores que pueden ser problemas de las funciones de servicios Web de Windows en el resultado de un error al ejecutar el comando.

-   [Parámetros out](#out-parameters)
-   [Códigos de error](#error-codes)
-   [Errores enriquecidos](#rich-errors)
-   [Errores y errores](#faults-and-errors)
-   [Información de error sensible al idioma](#language-sensitive-error-information)
-   [Códigos de error canónicos](#canonical-error-codes)
-   [Uso de API no válido](#invalid-api-usage)
-   [Seguridad](#security)

## <a name="out-parameters"></a>Parámetros out

Como norma general, el valor de los parámetros out no se modifica si se produce un error en una función.

Hay algunas instancias en las que se modifican los parámetros de salida si se produce un error en la función. Estos casos se indican explícitamente en la documentación de cada parámetro. Si la documentación no menciona nada sobre la modificación de los parámetros en caso de error, puede suponer de forma segura que la función no los modificará.

## <a name="error-codes"></a>Códigos de error

Todos los códigos de retorno de error son HRESULT. Esta API define un conjunto de Valores HRESULT en el \_ intervalo de servicios WebService, pero también devuelve errores definidos en otra parte de la API de Windows.

Consulte la documentación de la API específica para obtener información sobre qué códigos de error se devuelven. La lista no pretende ser exhaustiva para cada API, sino una lista de códigos de error para los que existen escenarios comunes de control explícito. Un llamador siempre debe suponer que otros códigos de error son posibles desde cualquier API.

Esta API define un número relativamente pequeño de códigos de error, que se corresponden con los escenarios en los que un programa desea tomar medidas en función del error. Los códigos de error por sí solos pueden no ser suficientes para determinar qué salió mal o para proporcionar una buena descripción del problema al usuario. La mejor comprensión del problema proviene de la utilización de errores enriquecidos, tal y como se describe a continuación.

## <a name="rich-errors"></a>Errores enriquecidos

Además de devolver un código de error, un llamador puede solicitar opcionalmente información de error para cualquier llamada API pasando un objeto de [ \_ error WS](ws-error.md) que no sea **null**. Para crear un objeto de error, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror). Si se produce un error, la API que causó el error rellenará el objeto de error con contexto adicional sobre la situación de error. Si no hay ningún error, el objeto de error no se modifica. Si se pasa un objeto de error **nulo** , indica que el autor de la llamada no está interesado en información de error enriquecida. Los destinatarios (incluidas las devoluciones de llamada) deben estar preparados para controlar los objetos de error **null** .

Tenga en cuenta que se puede usar el mismo objeto de error para varias llamadas API, pero solo se puede usar para una llamada de API a la vez (como es de subproceso único). Cada vez que se produce un error, se anexa información del error al objeto de error. Como una cadena de llamadas se desenreda, varias funciones pueden agregar información al objeto de error para proporcionar contexto adicional sobre el error. Para borrar el contenido del objeto de error antes de reutilizarlo (después de que se produzca un error), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Si no se produce ningún error, no es necesario restablecer el objeto de error antes de reutilizarlo.

La información de error enriquecida consta de lo siguiente:

-   Un conjunto de valores de propiedad, que proporcionan información adicional sobre el error, si está presente. Vea [**la \_ \_ propiedad WS error**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Cero o más cadenas de error. Las cadenas se agregan mediante [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)y se pueden consultar mediante el uso de [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring). El número de cadenas se puede consultar mediante [**el \_ \_ \_ \_ recuento de cadenas de propiedades de error de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Errores y errores

Consulte [errores](faults.md) para obtener información sobre cómo se relacionan los errores y los errores.

## <a name="language-sensitive-error-information"></a>Información de error sensible al idioma

Al crear un objeto de error, se especifica el LANGID de la traducción de idioma deseada para la información de error. Se utiliza al agregar información de error al objeto de error.

Este valor de idioma se puede recuperar o establecer mediante la [**propiedad de error de WS \_ \_ \_ LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="canonical-error-codes"></a>Códigos de error canónicos

Esta API proporciona un conjunto canónico de códigos de error (WS \_ E \_ \* ) que permiten usar diferentes tecnologías de comunicación sin tener que depender de los códigos de error específicos de la implementación subyacente concreta. Para obtener una lista completa de estos códigos de error, vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md).

Esto permite, por ejemplo, que un programa busque el punto de conexión WS E del código de error **\_ \_ \_ no encontrado si \_ se** usa TCP, UDP o http y realiza alguna acción (como intentar usar un punto de conexión diferente).

Cuando se asigna un código de error específico de la implementación a un error canónico, el código de error original se guarda en el objeto de error y todavía se puede tener acceso a él con fines de diagnóstico. Consulte [**el \_ \_ código de \_ \_ error original \_ de la propiedad WS error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) para obtener más información.

## <a name="invalid-api-usage"></a>Uso de API no válido

Los siguientes códigos de error se reservan para el uso no válido de la API y no se devolverán en otras circunstancias. Si se devuelve alguno de estos errores, puede ser una indicación de un error de aplicación.

-   **\_ \_ operación no válida de WS E \_**
-   **E \_ INVALIDARG**

Las enumeraciones siguientes forman parte del seguimiento:

-   [**identificador de la propiedad de error de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_código de excepción WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Los siguientes códigos de error forman parte del seguimiento:

-   **CERTIFICADO \_ E \_ CN \_ no \_ coincide**
-   **CERTIFICADO \_ E \_ caducado**
-   **CERT \_ E \_ UNTRUSTEDROOT**
-   **uso de CERT \_ E \_ incorrecto \_**
-   **CIFRAdo \_ E \_ revocación \_ sin conexión**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **\_Dirección WS \_ E \_ en \_ uso**
-   **\_Dirección WS \_ E \_ no \_ disponible**
-   **\_ \_ \_ acceso \_ denegado al extremo WS E**
-   **acción de punto de conexión de WS \_ E \_ \_ \_ no \_ admitida**
-   **\_extremo WS \_ E \_ desconectado**
-   **\_error de \_ punto de conexión WS E \_**
-   **\_error de \_ punto de conexión WS E \_ \_**
-   **\_extremo WS \_ E \_ no \_ disponible**
-   **\_ \_ \_ no \_ se encontró el punto de conexión WS E**
-   **el \_ punto de conexión WS E está \_ \_ demasiado \_ ocupado**
-   **\_extremo WS \_ E \_ inaccesible**
-   **\_ \_ \_ dirección URL del extremo no válida \_ de WS E**
-   **\_ \_ formato no válido de WS E \_**
-   **\_ \_ operación no válida de WS E \_**
-   **\_no se \_ \_ admite WS E**
-   **WS \_ E \_ no hay \_ traducción \_ disponible**
-   **\_ \_ desbordamiento numérico de WS E \_**
-   **error en el \_ objeto WS E \_ \_**
-   **\_operación WS \_ E \_ abandonada**
-   **\_operación WS \_ E \_ anulada**
-   **se \_ \_ \_ agotó el tiempo de \_ espera de la operación WS E**
-   **WS \_ E \_ otros**
-   **\_ \_ \_ acceso \_ denegado al proxy WS E**
-   **error de proxy de WS \_ E \_ \_**
-   **el \_ proxy WS E \_ \_ requiere \_ \_ autenticación básica**
-   **el \_ proxy WS E \_ \_ requiere \_ \_ autenticación implícita**
-   **el \_ proxy WS E \_ \_ requiere \_ Negotiate \_ auth**
-   **el \_ proxy WS E \_ \_ requiere \_ \_ autenticación NTLM**
-   **cuota de WS \_ E \_ \_ superada**
-   **\_ \_ \_ error del sistema de seguridad de WS E \_**
-   **el \_ token de seguridad de WS E \_ \_ \_ expiró**
-   **\_error de \_ comprobación de seguridad \_ \_ de WS E**
-   **WS \_ E \_ Server \_ requiere \_ \_ autenticación básica**
-   **WS \_ E \_ Server \_ requiere \_ \_ autenticación implícita**
-   **WS \_ E \_ Server \_ requiere \_ Negotiate \_ auth**
-   **WS \_ E \_ Server \_ requiere \_ \_ autenticación NTLM**
-   **Async de WS \_ S \_**
-   **fin de WS \_ S \_**

Las siguientes funciones forman parte del seguimiento:

-   [**identificador de la propiedad de error de WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_código de excepción WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

El siguiente identificador forma parte del seguimiento:

-   [ERROR de WS \_](ws-error.md)

La estructura siguiente forma parte del seguimiento:

-   [**\_propiedad WS error \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Seguridad

Hay una serie de consideraciones de seguridad que debe tener en cuenta el usuario del objeto de error:

-   El objeto de error puede contener datos que no son de confianza. Ejemplos de esto son: el error de WS \_ y las cadenas de error, que se pueden almacenar en el objeto de error basándose en la información recibida a través de un canal que no es de confianza. El usuario del objeto de error debe tener cuidado al inspeccionar la información del objeto de error y tomar decisiones basadas en sus valores.
-   Un usuario del objeto de error debe llamar a [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) después de inspeccionar la información sobre el error. Si no lo hace, puede producirse una acumulación de memoria.
-   Un usuario del objeto de error debe tener mucho cuidado al usar el \_ \_ \_ valor de la divulgación de errores de WS Full de la enumeración de la [**divulgación de \_ errores \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , porque el error generado podría contener información privada que se acumulaba como parte del proceso de registro de errores.

 

 




