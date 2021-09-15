---
title: Errors
description: En esta sección se describen los errores que pueden producirse Windows funciones de servicios web como resultado de un error al ejecutar el comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Errores de servicios web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360186"
---
# <a name="errors"></a>Errors

En esta sección se describen los errores que pueden producirse Windows funciones de servicios web como resultado de un error al ejecutar el comando.

-   [Parámetros de salida](#out-parameters)
-   [Códigos de error](#error-codes)
-   [Errores enriquecidos](#rich-errors)
-   [Errores y errores](#faults-and-errors)
-   [Información de error confidencial del lenguaje](#language-sensitive-error-information)
-   [Códigos de error canónicos](#canonical-error-codes)
-   [Uso de API no válido](#invalid-api-usage)
-   [Seguridad](#security)

## <a name="out-parameters"></a>Parámetros out

Como regla general, el valor de los parámetros out no se modifica si se produce un error en una función.

Hay algunas instancias en las que se modifican los parámetros out si se produce un error en la función. Estos casos se llaman explícitamente en la documentación de cada parámetro. Si la documentación no menciona nada sobre la modificación de parámetros en caso de error, puede suponer con seguridad que la función no los modificará.

## <a name="error-codes"></a>Códigos de error

Todos los códigos de retorno de error son HRESULT. Esta API define un conjunto de HRESULT en el intervalo FACILITY WEBSERVICES, pero también devuelve errores definidos en otra parte de Windows \_ API.

Consulte la documentación de API específicas para obtener información sobre qué códigos de error se devuelven. La lista no pretende ser exhaustiva para cada API, sino una lista de códigos de error para los que hay escenarios comunes para el control explícito. Un autor de la llamada siempre debe asumir que otros códigos de error son posibles desde cualquier API.

Esta API define un número relativamente pequeño de códigos de error, que corresponden a escenarios en los que un programa querrá realizar acciones basadas en el error. Los códigos de error por sí solos pueden no ser suficientes para determinar qué salió mal o para proporcionar una buena descripción del problema al usuario. La mejor comprensión del problema procede del uso de errores enriquecidos, como se describe a continuación.

## <a name="rich-errors"></a>Errores enriquecidos

Además de devolver un código de error, un autor de la llamada puedesolicitar opcionalmente información de error enriquecida para cualquier llamada API pasando un objeto[WS \_ ERROR](ws-error.md) que no sea NULL. Para crear un objeto de error, use [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror). Si se produce un error, la API que produjo el error rellenará el objeto de error con contexto adicional sobre la situación de error. Si no hay ningún error, el objeto de error no se modificará. Pasar un **objeto de** error NULL indica que el autor de la llamada no está interesado en la información de error enriquecida. Los destinatarios (incluidas las devoluciones de llamada) deben estar preparados para controlar los objetos de error **NULL.**

Tenga en cuenta que el mismo objeto de error se puede usar para varias llamadas API, pero solo se puede usar para una llamada API a la vez (ya que es un subproceso único). Cada vez que se produce un error, se anexa información de error al objeto de error. A medida que se desenreda una cadena de llamadas, varias funciones pueden agregar información al objeto de error para proporcionar contexto adicional sobre el error. Para borrar el contenido del objeto de error antes de volver a usarlo (después de que se produzca un error), use [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Si no se produce ningún error, no es necesario restablecer el objeto de error antes de volver a usarlo.

La información de error enriquecte consta de lo siguiente:

-   Conjunto de valores de propiedad, que proporcionan información adicional sobre el error si está presente. Vea [**WS \_ ERROR \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Cero o más cadenas de error. Las cadenas se agregan mediante [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)y se pueden consultar mediante [**WsGetErrorString.**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring) El número de cadenas se puede consultar mediante [**WS \_ ERROR PROPERTY STRING \_ \_ \_ COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Errores y errores

Consulte [Errores para obtener](faults.md) información sobre cómo se relacionan los errores y los errores.

## <a name="language-sensitive-error-information"></a>Información de error confidencial del lenguaje

Al crear un objeto de error, se especifica el LANGID de la traducción de idioma deseada para la información de error. Esto se usa al agregar información de error al objeto de error.

Este valor de lenguaje se puede recuperar o establecer mediante [**WS \_ ERROR PROPERTY \_ \_ LANGID.**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)

## <a name="canonical-error-codes"></a>Códigos de error canónicos

Esta API proporciona un conjunto canónico de códigos de error (WS E) que permiten usar diferentes tecnologías de comunicación sin tener que depender de los códigos de error específicos de la implementación \_ \_ \* subyacente específica. Para obtener una lista completa de estos códigos de error, [vea Windows valores devueltos de servicios web](windows-web-services-return-values.md).

Esto permite, por ejemplo, que un programa compruebe el código de error **WS \_ E ENDPOINT NOT \_ \_ \_ FOUND** si se usa TCP, UDP o HTTP, y realizar alguna acción (como intentar usar un punto de conexión diferente).

Cuando un código de error específico de implementación se asigna a un error canónico, el código de error original se guarda en el objeto de error y todavía se puede acceder a él con fines de diagnóstico. Vea [**CÓDIGO DE ERROR ORIGINAL DE WS \_ ERROR \_ PROPERTY \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) para obtener más información.

## <a name="invalid-api-usage"></a>Uso de API no válido

Los siguientes códigos de error están reservados para el uso de API no válido y no se devolverán en otras circunstancias. Si se devuelve cualquiera de estos errores, puede ser una indicación de un error de aplicación.

-   **WS \_ E OPERACIÓN NO \_ \_ VÁLIDA**
-   **E \_ INVALIDARG**

Las enumeraciones siguientes forman parte del seguimiento:

-   [**WS \_ ERROR \_ PROPERTY \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**CÓDIGO DE \_ EXCEPCIÓN DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Los siguientes códigos de error forman parte del seguimiento:

-   **CERT \_ E \_ CN \_ NO \_ MATCH**
-   **CERTIFICADO \_ E \_ EXPIRADO**
-   **CERT \_ E \_ UNTRUSTEDROOT**
-   **USO \_ INCORRECTO DE CERT E \_ \_**
-   **REVOCACIÓN \_ DE CRYPT E \_ SIN \_ CONEXIÓN**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **DIRECCIÓN DE WS \_ E \_ EN \_ \_ USO**
-   **WS \_ E \_ ADDRESS \_ NOT \_ AVAILABLE**
-   **ACCESO AL PUNTO DE CONEXIÓN DE WS \_ E \_ \_ \_ DENEGADO**
-   **NO SE ADMITE LA ACCIÓN DE PUNTO DE CONEXIÓN DE WS \_ \_ \_ \_ \_ E**
-   **PUNTO DE CONEXIÓN DE WS \_ E \_ \_ DESCONECTADO**
-   **ERROR DE PUNTO DE CONEXIÓN DE WS \_ E \_ \_**
-   **ERROR DE PUNTO DE CONEXIÓN DE WS \_ E \_ \_ \_ RECIBIDO**
-   **PUNTO DE CONEXIÓN DE WS \_ E \_ NO \_ \_ DISPONIBLE**
-   **PUNTO DE CONEXIÓN DE WS \_ E \_ NO \_ \_ ENCONTRADO**
-   **PUNTO DE CONEXIÓN \_ WS E \_ DEMASIADO \_ \_ OCUPADO**
-   **PUNTO DE CONEXIÓN DE WS \_ E \_ \_ INACCESIBLE**
-   **WS \_ E DIRECCIÓN URL DEL PUNTO DE CONEXIÓN NO \_ \_ \_ VÁLIDO**
-   **WS \_ E FORMATO NO \_ \_ VÁLIDO**
-   **WS \_ E OPERACIÓN NO \_ \_ VÁLIDA**
-   **WS \_ E NO SE \_ \_ ADMITE**
-   **WS \_ E \_ NO \_ TRANSLATION \_ AVAILABLE**
-   **WS \_ E \_ NUMERIC \_ OVERFLOW**
-   **ERROR DEL OBJETO WS \_ E \_ \_**
-   **OPERACIÓN \_ DE WS E \_ \_ ABANDONED**
-   **WS \_ E \_ OPERATION \_ ABORTED**
-   **TIEMPO DE \_ ESPERA DE LA OPERACIÓN \_ \_ WS E \_**
-   **WS \_ E \_ OTHER**
-   **ACCESO DE PROXY DE WS \_ E \_ \_ \_ DENEGADO**
-   **ERROR DE PROXY DE WS \_ E \_ \_**
-   **EL PROXY \_ WS E \_ REQUIERE \_ \_ \_ AUTENTICACIÓN BÁSICA**
-   **EL PROXY DE WS \_ E \_ REQUIERE \_ \_ \_ AUTENTICACIÓN IMPLÍCITA**
-   **EL PROXY \_ WS E \_ REQUIERE LA \_ \_ \_ AUTENTICACIÓN NEGOTIATE**
-   **EL PROXY DE WS \_ E \_ REQUIERE \_ \_ \_ AUTENTICACIÓN NTLM**
-   **CUOTA DE WS \_ E \_ \_ SUPERADA**
-   **ERROR DEL \_ SISTEMA \_ DE \_ SEGURIDAD \_ WS E**
-   **TOKEN DE SEGURIDAD DE WS \_ E \_ \_ \_ EXPIRADO**
-   **ERROR DE \_ COMPROBACIÓN \_ DE SEGURIDAD \_ DE \_ WS E**
-   **WS \_ E SERVER REQUIERE \_ \_ \_ \_ AUTENTICACIÓN BÁSICA**
-   **EL SERVIDOR \_ WS E \_ REQUIERE \_ \_ \_ AUTENTICACIÓN IMPLÍCITA**
-   **WS \_ E SERVER REQUIERE LA \_ \_ \_ \_ AUTENTICACIÓN NEGOTIATE**
-   **WS \_ E SERVER REQUIERE \_ \_ \_ AUTENTICACIÓN \_ NTLM**
-   **WS \_ S \_ ASYNC**
-   **WS \_ S \_ END**

Las siguientes funciones forman parte del seguimiento:

-   [**IDENTIFICADOR DE \_ PROPIEDAD \_ DE ERROR DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**CÓDIGO DE \_ EXCEPCIÓN DE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

El siguiente identificador forma parte del seguimiento:

-   [ERROR \_ DE WS](ws-error.md)

La siguiente estructura forma parte del seguimiento:

-   [**WS \_ ERROR \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Seguridad

Hay una serie de consideraciones de seguridad que el usuario del objeto de error debe tener en cuenta:

-   El objeto de error puede contener datos que no son de confianza. Algunos ejemplos de esto son: el error de WS y las cadenas de error, que se pueden almacenar en el objeto de error en función de la información recibida a través de un canal que no \_ es de confianza. El usuario del objeto de error debe tener cuidado al inspeccionar la información del objeto de error y tomar decisiones basadas en sus valores.
-   Un usuario del objeto de error debe llamar a [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) después de inspeccionar la información sobre el error. Si no lo hace, puede provocar una acumulación de memoria.
-   Un usuario del objeto de error debe tener mucho cuidado al usar el valor WS FULL FAULT DISCLOSURE de la enumeración \_ \_ \_ [**WS \_ FAULT \_ DISCLOSURE,**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) ya que el error generado podría contener información privada que se acumuló como parte del proceso de registro de errores.

 

 




