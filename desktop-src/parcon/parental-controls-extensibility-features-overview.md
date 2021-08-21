---
description: Los controles parentales se pueden extender mediante la configuración y las API de registro.
ms.assetid: f0fc1b11-6de4-48f6-afc9-f05c8812d2bd
title: Información general sobre las características de extensibilidad de los controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bf609c08a4114d7d96ae600744879bda53ac483d90bcd25def3dd0d5f9e3c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971724"
---
# <a name="parental-controls-extensibility-features-overview"></a>Información general sobre las características de extensibilidad de los controles parentales

Los controles parentales se pueden extender mediante la configuración y las API de registro.

-   [Registro: en segundo plano](/windows)
-   [Extensibilidad del registro](#logging-extensibility)
-   [Incorporación de vínculos de extensibilidad de la interfaz de usuario general del Panel de controles parentales](#parental-controls-panel-general-ui-extensibility-link-addition)
-   [Reemplazo de filtro de contenido web](#web-content-filter-replacement)

## <a name="loggingbackground"></a>Registro: en segundo plano

Microsoft ha definido una serie de eventos estándar para abordar actividades comunes:

-   Sistema: cambios en la configuración de los controles parentales, cambios en la cuenta, cambio del reloj del sistema, intentos de inicio de sesión con errores.
-   User:
    -   Límites de tiempo/sistema: horas de inicio de sesión, cierre de sesión, intentos de ejecución de la aplicación y duración de ejecución de la aplicación (consulte la nota).
    -   Restricciones web: sitios web visitados y bloqueados, intentos de descarga de archivos. Los exploradores web y las aplicaciones de tipo explorador no necesitan registrar estos registros, ya que el LSP del filtro de contenido web lo hace. Los filtros web de reemplazo tendrían que generar estos eventos.
    -   Juegos: juegos reproducidos y bloqueados, final del juego (los eventos juntos proporcionan la duración reproducida).
    -   Permitir y bloquear programas específicos: intento de ejecución, apagado, bloqueado por restricciones generales de aplicaciones.
    -   Mensajería instantánea: intento de iniciación de conversión, intento de combinación de conversación, permiso de conversación, vídeo/audio/juego/servicio de mensajes corto/transferencia de archivos/característica de intercambio de direcciones URL, intento de cambio de lista de contactos.
    -   Correo electrónico: recibido o recibido bloqueado, intento de envío, intento de cambio de lista de contactos.
    -   Medios: medios reproducdos e intentados.

No todos los eventos anteriores son adecuados para su uso por parte de las aplicaciones. Los cambios en la cuenta, el cambio del reloj del sistema y el registro de eventos de inicio y cierre de sesión solo los implementa el sistema operativo, por lo que no se exponen públicamente.

> [!Note]  
> La instrumentación de eventos de entrada y salida de la aplicación está disponible en Windows Vista y se configura mediante controles parentales para registrar estos datos.

 

## <a name="logging-extensibility"></a>Extensibilidad del registro

Un evento personalizado genérico también se define con tres etiquetas o valores disponibles, por lo que los ISV normalmente no tendrán que definir los suyos propios en un manifiesto. El Visor de registros reconocerá y mostrará los encabezados y valores de etiqueta si el número de campos usados (de 1 a 3) y los encabezados de cada campo se registran mediante la API WMI. La configuración Visor de eventos también se puede usar para ver eventos personalizados.

Si el evento personalizado genérico no es adecuado, un ISV puede definir su propio mediante un manifiesto de aplicación y puede registrar encabezados para hasta tres campos mediante la misma API WMI.

Los ISV pueden optar por definir sus propios eventos y consumirlos independientemente del Visor de registros a través de Windows API. Esto no tiene la ventaja de la centralización completa del registro.

## <a name="parental-controls-panel-general-ui-extensibility-link-addition"></a>Incorporación de vínculos de extensibilidad de la interfaz de usuario general del Panel de controles parentales

Un vínculo de extensibilidad de la interfaz de usuario de uso general se expone mediante el acceso a la configuración a través de WMI, la creación de una instancia de extensión a partir de la ruta de acceso y el identificador del archivo DLL del recurso de nombre pasados, la ruta de acceso de imagen (mapa de bits), la ruta de acceso de la imagen de estado deshabilitada (mapa de bits), la ruta de acceso de dll del recurso de subtítulos y las especificaciones de ruta de acceso ejecutable. Una vez registrado, el vínculo aparecerá en el área Más Configuración del Panel de controles parentales y, al hacer clic en él, se invocará el ejecutable especificado.

La cadena de ruta de acceso ejecutable puede incluir opcionalmente un token para que el SID del usuario actual se sustituya antes de la invocación. Esto permite que la ejecución del vínculo funcione en el contexto del usuario para el que se está viendo actualmente la página central, si el ejecutable necesita conocer el SID.

## <a name="web-content-filter-replacement"></a>Reemplazo de filtro de contenido web

Como se indicó en el tema Control [parental In-Box restricciones](parental-controls-in-box-restrictions-and-user-interfaces.md)e interfaces de usuario , el filtro de contenido web incluido se puede reemplazar por un filtro proporcionado por el proveedor. Esto se realiza mediante el acceso a la configuración a través de WMI para establecer un GUID y un nombre que posee el filtrado.

El mecanismo general de extensibilidad de la interfaz de usuario se usa para exponer un filtro de terceros. Se trata del mismo mecanismo que se usa para cualquier extensión que quiera aparecer en la sección Más Configuración de la sección Parental de nivel superior Panel de control. Si se toma el paso adicional de establecer el mismo GUID y una ruta de acceso de DLL de recursos de nombre adecuada en la configuración de filtro de nivel de sistema, se ocultará el vínculo de filtro mostrado en el cuadro y se mostrará la entrada de terceros en la parte superior de la sección Más Configuración. El nombre registrado para el filtro se mostrará en la sección de resumen.

Al restablecer la configuración de GUID y ruta de acceso de nombre o identificador de filtro, el filtro de contenido web de cuadro se restablecerá como filtro activo y aparecerá de nuevo en la sección Windows Configuración.

Tenga en cuenta que los filtros de terceros no están restringidos en las tecnologías que se usan para conectarse a Windows comunicaciones. Un filtro simplemente debe exponer su configuración mediante un vínculo de extensibilidad y respetar la configuración adecuada de los controles parentales.

 

 
