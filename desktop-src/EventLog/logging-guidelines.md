---
description: Los registros de eventos almacenan registros de eventos importantes en nombre del sistema y de las aplicaciones que se ejecutan en el sistema.
ms.assetid: 58a6569a-2775-4687-bf99-579fa4153191
title: Instrucciones de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1210757a7961d82d13d4887e40fbd3837b86138
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156161"
---
# <a name="logging-guidelines"></a>Instrucciones de registro

Los registros de eventos almacenan registros de eventos importantes en nombre del sistema y de las aplicaciones que se ejecutan en el sistema. Dado que las funciones de registro son de uso general, debe decidir qué información es adecuada para el registro. Por lo general, solo debe registrar información que pueda ser útil para diagnosticar un problema de hardware o software. El registro de eventos no está diseñado para usarse como herramienta de seguimiento.

## <a name="choosing-events-to-log"></a>Elegir eventos para registrar

A continuación se muestran ejemplos de casos en los que el registro de eventos puede ser útil:

-   Problemas de recursos. El registro de un evento de advertencia cuando se produce un error en la asignación de memoria puede ayudar a indicar la causa de una situación de memoria insuficiente.
-   Problemas de hardware. Si un controlador de dispositivo detecta un tiempo de espera de controlador de disco, un error de alimentación en un puerto paralelo o un error de datos de una tarjeta de red o serie, el controlador de dispositivo puede registrar información acerca de estos eventos para ayudar al administrador del sistema a diagnosticar problemas de hardware.
-   Sectores dañados. Si un controlador de disco detecta un sector no válido, es posible que pueda leer o escribir en el sector después de volver a intentar la operación, pero el sector dejará de ser correcto. Si el controlador de disco puede continuar, debe registrar un evento de advertencia. de lo contrario, debe registrar un evento de error. Si un controlador del sistema de archivos encuentra un gran número de sectores dañados y los corrige, el registro de eventos de advertencia puede ayudar a que un Administrador determine que el disco puede estar a punto de producir un error.
-   Eventos de información. Una aplicación de servidor (por ejemplo, un servidor de base de datos) registra un usuario que inicia sesión, abre una base de datos o inicia una transferencia de archivos. El servidor también puede registrar otros eventos, como errores (no puede tener acceso al archivo, el proceso de host está desconectado, etc.), daños en la base de datos o si una transferencia de archivos se realizó correctamente.

## <a name="writing-messages"></a>Escribir los mensajes

Los mensajes deben tener sentido para los administradores y los usuarios que intentan solucionar un problema. Un mensaje debe contener toda la información necesaria para comprender la causa del problema y cómo corregirlo.

Evite escribir un mensaje críptico como "un paquete de controladores recibido del subsistema de e/s no era válido. Los datos son el paquete. " Un mensaje mejor indicaría que el controlador en cuestión funciona correctamente, pero está registrando paquetes con formato incorrecto. Podría indicar que se necesita una versión Unicode del controlador para corregir el problema. Para obtener más información sobre la escritura de mensajes de error correctos, vea instrucciones sobre los [mensajes de error](/windows/desktop/Debug/error-message-guidelines).

No use tabulaciones ni comas en el texto del mensaje, ya que los registros de eventos se pueden guardar como archivos de texto separados por comas o por tabulaciones. Muchas organizaciones importan estos archivos en las bases de datos y los caracteres de formato adicionales requerirán manipulación manual.

Al utilizar nombres UNC u otros vínculos que contengan espacios, incluya el nombre entre corchetes angulares. Por ejemplo, <\\ \\ *ShareName* \\ *ServerName*>. Puede escribir una dirección URL al final del mensaje que dirige al usuario al material de ayuda relacionado. La dirección URL debe ser un nombre de host DNS completo. Por ejemplo, puede anexar el siguiente texto a los mensajes: "para obtener información adicional sobre este mensaje, visite el sitio de soporte técnico en https://www.microsoft.com/Support/ProdRedirect/ContentSearch.asp ". El vínculo conduce a una página ASP que redirige al usuario al contenido relacionado con el mensaje de error. Analizaría parámetros adicionales (que se pasaron al hacer clic en la dirección URL) para determinar dónde redirigir al usuario.

Los argumentos que se pasan a la función [**ReportEvent**](/windows/desktop/api/Winbase/nf-winbase-reporteventa) se anexan a la dirección URL de la siguiente manera:

``` syntax
strHTTPQuery += L"?EvtSrc=" + _strEscapedSource;
strHTTPQuery += L"&EvtCat=" + _strEscapedCategory;
strHTTPQuery += L"&EvtID=" + _strEscapedEventID;
strHTTPQuery += L"&EvtCatID=" + _strEscapedCategoryID;
strHTTPQuery += L"&EvtType=" + _strEscapedType;
strHTTPQuery += L"&EvtTypeID=" + _strEscapedTypeID;
strHTTPQuery += L"&EvtRptTime=" + _strEscapedDateAndTime;
strHTTPQuery += L"&EvtTZBias=" + _strEscapedTimeZoneBias;
```

Si el nombre de la compañía, el nombre del producto, la versión del producto, el nombre de archivo y la versión del archivo del encabezado DLL del mensaje son válidos, también se anexan a la dirección URL:

``` syntax
ADD_VER_STR(L"CoName",   _strEscapedCompanyName);
ADD_VER_STR(L"ProdName", _strEscapedProductName);
ADD_VER_STR(L"ProdVer",  _strEscapedProductVersion);
ADD_VER_STR(L"FileName", _strEscapedFileName);
ADD_VER_STR(L"FileVer",  _strEscapedFileVersion);
```

## <a name="reducing-overhead"></a>Reducción de la sobrecarga

El registro de eventos consume recursos como el espacio en disco y el tiempo de procesador. La cantidad de espacio en disco que requiere un registro de eventos y la sobrecarga de una aplicación que registra eventos dependen de la cantidad de información que decida registrar. Esta es la razón por la que es importante registrar solo la información esencial. También es conveniente colocar las llamadas de registro de eventos en una ruta de acceso de error en el código en lugar de en la ruta de acceso del código principal, lo que reduciría el rendimiento.

La cantidad de espacio en disco necesario para cada entrada del registro de eventos incluye los miembros de la estructura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) . Se trata de una estructura de longitud variable; las cadenas y los datos binarios se almacenan después de la estructura.

 

 
