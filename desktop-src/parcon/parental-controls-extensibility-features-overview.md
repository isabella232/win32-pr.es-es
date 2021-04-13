---
description: Los controles parentales se pueden extender mediante la configuración y las API de registro.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Información general sobre las características de extensibilidad de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe150c5955881b8038cdca9a1e4562ee28093f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361420"
---
# <a name="parental-controls-extensibility-features-overview"></a>Información general sobre las características de extensibilidad de controles parentales

Los controles parentales se pueden extender mediante la configuración y las API de registro.

-   [Registro: fondo](/windows)
-   [Extensibilidad de registro](#logging-extensibility)
-   [Panel de control parental adición de vínculos de extensibilidad de IU general](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Reemplazo de filtro de contenido web](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Registro: fondo

Microsoft ha definido varios eventos estándar para abordar actividades comunes:

-   Sistema: cambios de configuración de controles parentales, cambios de cuenta, cambio de reloj del sistema, intentos de inicio de sesión incorrectos.
-   User:
    -   Límites de sistema/tiempo: horas de inicio de sesión, cierre de sesión, intentos de ejecución de aplicaciones y duración de la ejecución de la aplicación (vea la nota).
    -   Restricciones Web: sitios web visitados y bloqueados, intentos de descarga de archivos. No es necesario que los exploradores Web y las aplicaciones de tipo explorador se registren, ya que el administrador de contenido web lo hace. Los filtros Web de reemplazo deben generar estos eventos.
    -   Juegos: juegos reproducidos y bloqueados, el final del juego (eventos juntos proporcionan la duración reproducida).
    -   Permitir y bloquear programas específicos: ejecutar intento, apagado, bloqueado por restricciones de aplicación generales.
    -   Mensajería instantánea: intento de iniciación de conversión, intento de combinación de conversación, salida de conversación, vídeo/audio/juego/Short Message Service/transferencia de archivos/característica de intercambio de direcciones URL, intento de cambio de lista de contactos.
    -   Correo electrónico: intento de recepción o recepción bloqueada, intento de envío y cambio de la lista de contactos.
    -   Multimedia: multimedia reproducida e intentada.

No todos los eventos anteriores son adecuados para que las usen las aplicaciones. Los cambios de cuenta, el cambio de reloj del sistema y el registro de eventos de inicio y cierre de sesión solo los implementa el sistema operativo, por lo que no se exponen públicamente.

> [!Note]  
> La instrumentación de eventos de entrada y salida de la aplicación está disponible en Windows Vista y está configurada por controles parentales para registrar estos datos.

 

## <a name="logging-extensibility"></a>Extensibilidad de registro

Un evento personalizado genérico también se define con 3 etiquetas/valores disponibles, por lo que los ISV normalmente no necesitan definir sus propios en un manifiesto. El visor de registros reconocerá y mostrará los encabezados y valores de etiqueta si el número de campos usados (1 a 3) y los encabezados de cada campo se registran mediante la API de WMI. El Visor de eventos genérico también puede usarse para ver eventos personalizados.

Si el evento personalizado genérico no es adecuado, un ISV puede definir su propio mediante un manifiesto de aplicación y puede registrar encabezados para hasta tres campos mediante la misma API de WMI.

Los ISV pueden optar por definir sus propios eventos y consumirlos independientemente del visor de registros a través de las API de Windows públicas. Esto no tiene la ventaja de que la centralización del registro está completa.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Panel de control parental adición de vínculos de extensibilidad de IU general

Un vínculo de extensibilidad de la interfaz de usuario de uso general se expone mediante el acceso a la configuración a través de WMI, la creación de una instancia de extensión a partir de la ruta de acceso del recurso nombre DLL ruta e identificador, ruta de acceso de imagen Tras su registro, el vínculo aparecerá en el área más configuraciones del panel Controles parentales y, al hacer clic en él, se invocará el archivo ejecutable especificado.

Opcionalmente, la cadena de ruta de acceso ejecutable puede incluir un token para el SID del usuario actual que se sustituirá antes de la invocación. Esto permite que la ejecución del vínculo funcione en el contexto del usuario para el que se está viendo la página del concentrador actualmente, si el ejecutable necesita conocer el SID.

## <a name="web-content-filter-replacement"></a>Reemplazo de filtro de contenido web

Como se indicó en el tema [control parental In-Box restricciones e interfaces de usuario](parental-controls-in-box-restrictions-and-user-interfaces.md), el filtro de contenido Web incorporado se puede reemplazar por un filtro proporcionado por el proveedor. Esto se realiza mediante el acceso a la configuración a través de WMI para establecer un GUID y el nombre que posee el filtrado.

El mecanismo general de extensibilidad de la interfaz de usuario se usa para exponer un filtro de terceros. Este es el mismo mecanismo que se usa para cualquier extensión que desee que aparezca en la sección más configuraciones del panel de control parental de nivel superior. Realizar el paso adicional de establecer el mismo GUID y un identificador y ruta de acceso de la DLL de recursos de nombre apropiados en la configuración del filtro de nivel de sistema hará que el vínculo de filtro mostrado en la caja esté oculto y la entrada de otro fabricante se muestre en la parte superior de la sección más configuraciones. El nombre registrado para el filtro se mostrará en la sección Resumen.

Al restablecer el GUID del filtro y la configuración de la ruta de acceso del nombre y el identificador, el filtro de contenido Web incorporado se volverá a establecer como filtro activo y aparecerá de nuevo en la sección configuración de Windows.

Tenga en cuenta que los filtros de terceros no están limitados en las tecnologías que se usan para conectarse a las comunicaciones de Windows. Un filtro solo debe exponer su configuración mediante un vínculo de extensibilidad y seguir la configuración apropiada de los controles parentales.

 

 
