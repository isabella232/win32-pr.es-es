---
description: Los elementos principales de la información que proporciona una aplicación para iniciar una sesión de comunicaciones son el tipo de dirección, el tipo de medio o los tipos y la dirección de destino.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Iniciar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e925ba90460b88c85a9aab1624923acdbc4572a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908594"
---
# <a name="initiate-a-session"></a>Iniciar una sesión

Los elementos principales de la información que proporciona una aplicación para iniciar una sesión de comunicaciones son el [tipo de dirección](address-type-ovr.md), el [tipo de medio](media-type-ovr.md) o los tipos y la [Dirección](address-ovr.md)de destino.

La dirección de destino puede requerir la [traducción de direcciones](#address-translation) para poner la información especificada por un usuario en el formato adecuado para un tipo de dirección determinado. Por ejemplo, un número de teléfono que se encontraba en una libreta de direcciones electrónicas en formato [canónico](address-ovr.md) necesitará la traducción al formato de [marcado](address-ovr.md) .

Algunas sesiones pueden requerir parámetros de configuración especiales, si son compatibles con el proveedor de servicios. Por ejemplo, un TSP de RDSI puede transmitir información de usuario y algunos MSP requieren información sobre la dirección del flujo de medios. Consulte la [información](session-information-ovr.md) de la sesión para ver una revisión de los datos que se pueden establecer u obtener relativos a una sesión.

Una vez iniciada una sesión, TAPI informará a la aplicación del progreso de la llamada mediante el mecanismo de notificación de eventos configurado durante la inicialización.

**TAPI 2. x:** Las aplicaciones inician una sesión mediante la función [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) . La función [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) se usa para realizar la traducción de direcciones, si es necesario.

Los parámetros de configuración de llamada se pueden almacenar en la estructura de datos [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) y, a continuación, se usa un puntero a esta estructura como parámetro de [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall). Si no se proporciona ninguna estructura **LINECALLPARAMS** a **lineMakeCall**, se solicita una llamada de nivel de voz de Pots predeterminada con un conjunto de valores predeterminados.

Si la sesión se ha configurado correctamente, se devuelve un identificador de llamada con [privilegios](privilege-ovr.md) de *propietario* a la aplicación y TAPI envía la línea de aplicación [**\_ CALLSTATE**](./line-callstate.md) mensajes con información sobre el progreso de la llamada. Normalmente, las aplicaciones usan estos mensajes para mostrar informes de estado al usuario.

**TAPI 3. x:** Las aplicaciones inician una sesión de comunicaciones mediante la invocación del método [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) en una dirección capaz de controlar el tipo de dirección y el tipo de medio necesario. Si la dirección expone la interfaz [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) , se seleccionan los terminales en los flujos multimedia del objeto de llamada. Vea el ejemplo de creación de código de [llamada](make-a-call.md) para ver una ilustración de este proceso.

Los parámetros de configuración de llamada se pueden almacenar o cambiar mediante métodos expuestos por la interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

Si la sesión se configura correctamente, TAPI devuelve un puntero de la interfaz [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) que se puede usar para operaciones de sesión adicionales o para obtener un puntero de interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) que se puede usar para adquirir información de sesión adicional. La interfaz [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) procesa los eventos de estado de llamada TAPI.

> [!Note]  
> TAPI no se debe utilizar para las transmisiones de fax. En su lugar, use las funciones disponibles a través de MAPI, la API de mensajería de Microsoft.

 

## <a name="address-translation"></a>Traducción de direcciones

Una aplicación de servidor o de usuario final puede almacenar direcciones en un formato que no sea compatible con las necesidades de un proveedor de servicios determinado. Por ejemplo, un número de teléfono puede almacenarse en una libreta de direcciones electrónicas en [formato canónico](address-ovr.md), pero la mayoría de los proveedores de servicios que controlan los números de teléfono requieren el [formato de marcado](address-ovr.md).

TAPI proporciona operaciones de traducción de direcciones que ayudan a una aplicación a presentar el tipo de dirección correcto a un TSP. El proveedor de servicios especifica en TAPI los tipos de dirección que admite y no necesita incluir ningún tipo de traducción de direcciones.

**TAPI 2. x:** Vea [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Vea [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Listas de peajes

En algunas ubicaciones de Norteamérica, todas las llamadas telefónicas que se colocan en el código de área local son llamadas locales. En otras ubicaciones, algunas llamadas que se colocan en el código de área local son de larga distancia y necesitan que se marque un prefijo "1". Los tres primeros dígitos de la dirección (el prefijo) determinan si una llamada en el código de área local es una llamada de peaje.

Una *lista de llamadas* es una lista de prefijos en el código de área local cuyas direcciones deben marcarse como direcciones de larga distancia y se han evaluado los cargos de larga distancia.

Las listas de llamadas no son relevantes para los proveedores de servicios o para las aplicaciones que no tienen acceso a una red telefónica.

**TAPI 2. x:** Vea [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ INTOLLLIST y LINETRANSLATERESULT \_ NOTINTOLLLIST bits en la estructura [**LINETRANSLATEOUTPUT**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) ), [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Vea [**ITAddressTranslation:: TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo:: get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
