---
description: Los elementos principales de información que proporciona una aplicación para iniciar una sesión de comunicaciones son el tipo de dirección, el tipo o los tipos de medios y la dirección de destino.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Iniciar una sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0226fc1b04ea5859bc4a96b6f5ca43e3749e7664a9ccf6810b586115171530b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975855"
---
# <a name="initiate-a-session"></a>Iniciar una sesión

Los elementos principales de información que proporciona una aplicación para [](media-type-ovr.md) iniciar una sesión de comunicaciones son el tipo de dirección [,](address-type-ovr.md)el tipo de medio o los tipos y la dirección de [destino](address-ovr.md).

La dirección de destino puede requerir [traducción de direcciones](#address-translation) para poner la información especificada por un usuario en el formato adecuado para un tipo de dirección determinado. Por ejemplo, un número de teléfono que estaba en una libreta de direcciones electrónica en formato [canónico](address-ovr.md) requerirá la traducción al [formato dialable.](address-ovr.md)

Algunas sesiones pueden requerir parámetros de configuración especiales, si el proveedor de servicios lo admite. Por ejemplo, un TSP de ISDN puede transmitir información de usuario y algunos MSP requieren información sobre la dirección del flujo multimedia. Consulte [Información de sesión](session-information-ovr.md) para obtener una revisión de los datos que se pueden establecer u obtener en relación con una sesión.

Una vez iniciada una sesión, TAPI informará a la aplicación del progreso de la llamada mediante el mecanismo de notificación de eventos configurado durante la inicialización.

**TAPI 2.x:** Las aplicaciones inician una sesión mediante [**la función lineMakeCall.**](/windows/win32/api/tapi/nf-tapi-linemakecall) La [**función lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) se usa para realizar la traducción de direcciones, si es necesario.

Los parámetros de instalación de llamadas se pueden almacenar en la estructura de datos [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) y, a continuación, se usa un puntero a esta estructura como parámetro [**de lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall). Si no se proporciona ninguna estructura **LINECALLPARAMS** a **lineMakeCall**, se solicita una llamada predeterminada de nivel de voz de POTS con un conjunto de valores predeterminados.

Si la sesión se configura correctamente,  se devuelve un identificador de llamada con [privilegios](privilege-ovr.md) de propietario a la aplicación y TAPI envía los mensajes [**LINE \_ CALLSTATE**](./line-callstate.md) de la aplicación con información sobre el progreso de la llamada. Las aplicaciones suelen usar estos mensajes para mostrar informes de estado al usuario.

**TAPI 3.x:** Las aplicaciones inician una sesión de comunicaciones invocando el método [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) en una dirección capaz de controlar el tipo de dirección y el tipo de medio necesarios. Si la dirección expone la [**interfaz ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) los terminales se seleccionan en los flujos multimedia del objeto de llamada. Vea el [ejemplo de código Crear](make-a-call.md) una llamada para obtener una ilustración de este proceso.

Los parámetros de instalación de llamadas se pueden almacenar o cambiar mediante métodos expuestos [**por la interfaz ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

Si la sesión se configura correctamente, TAPI devuelve un puntero de interfaz [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) que se puede usar para operaciones de sesión adicionales, o para obtener un puntero de interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) que se puede usar para adquirir información de sesión adicional. La [**interfaz ITCallStateEvent procesa**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) eventos de estado de llamada TAPI.

> [!Note]  
> TAPI no debe usarse para las transmisiones de fax. En su lugar, use las funciones disponibles a través de MAPI, Mensajes de Microsoft API.

 

## <a name="address-translation"></a>Traducción de direcciones

Una aplicación de servidor o usuario final puede almacenar direcciones en un formato que no sea compatible con las necesidades de un proveedor de servicios determinado. Por ejemplo, un número de teléfono se [](address-ovr.md)puede almacenar en una libreta de direcciones electrónica en formato canónico, pero la mayoría de los proveedores de servicios que administran números de teléfono requieren el [formato de marcado](address-ovr.md).

TAPI proporciona operaciones de traducción de direcciones que ayudan a una aplicación a presentar el tipo de dirección correcto a un TSP. El proveedor de servicios especifica a TAPI qué tipos de direcciones admite y no necesita incluir ninguna forma de traducción de direcciones.

**TAPI 2.x:** Vea [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Vea [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Listas de peaje

En algunas ubicaciones de Norteamérica, todas las llamadas telefónicas realizadas al código de área local son llamadas locales. En otras ubicaciones, algunas llamadas realizadas al código de área local son de larga distancia y necesitan que se marque un prefijo "1". Los tres primeros dígitos de la dirección (el prefijo) determinan si una llamada dentro del código de área local es o no una llamada de peaje.

Una *lista de peajes* es una lista de prefijos en el código de área local cuyas direcciones se deben marcar como direcciones de larga distancia y se evalúan los cargos de larga distancia.

Las listas de peaje no son relevantes para los proveedores de servicios ni para las aplicaciones que no tienen acceso a una red telefónica.

**TAPI 2.x:** Vea los bits [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ INTOLLLIST y LINETRANSLATERESULT NOTINTOLLLIST en la estructura \_ [**LINETRANSLATEOUTPUT),**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Vea [**ITAddressTranslation::TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo::get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
