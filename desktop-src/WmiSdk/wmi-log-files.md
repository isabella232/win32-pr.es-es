---
description: WMI usa seguimiento de eventos (ETW) y los eventos se pueden obtener a través de la interfaz Visor de eventos usuario o la herramienta de línea de comandos Wevtutil. Para obtener más información, vea Seguimiento de la actividad WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Archivos de registro WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359206"
---
# <a name="wmi-log-files"></a>Archivos de registro WMI

WMI usa [seguimiento de](/windows/desktop/ETW/event-tracing-portal) eventos (ETW) y  los eventos se pueden obtener a través de la interfaz Visor de eventos usuario o la herramienta de línea de comandos Wevtutil. Para obtener más información, vea [Seguimiento de la actividad WMI](tracing-wmi-activity.md).

-   [Seguimiento de eventos en lugar de registros de texto](#event-tracing-instead-of-text-logs)
-   [Archivos de registro WMI](#wmi-log-files)
-   [Temas relacionados](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Seguimiento de eventos en lugar de registros de texto

La actividad del servicio WMI se registra en el archivo WMITracing.log. Para obtener más información sobre cómo habilitar el seguimiento de eventos WMI y obtener acceso al archivo WMITracing.log, vea [Seguimiento de la actividad WMI](tracing-wmi-activity.md). Windows Los proveedores del modelo de controlador (WDM) continúan iniciando sesión en el archivo Wbemprov.log.

## <a name="wmi-log-files"></a>Archivos de registro WMI

El servicio WMI y algunos proveedores escriben archivos de registro de texto para registrar eventos.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Archivos de registro del proveedor WMI](wmi-provider-log-files.md)
</dt> <dd>

Los proveedores WMI también pueden mantener registros. Los archivos de registro que aparecen en un sistema dependen de qué proveedores estén instalados.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Actividad WMI de seguimiento](tracing-wmi-activity.md)
</dt> <dt>

[Actividad WMI de registro](logging-wmi-activity.md)
</dt> </dl>

 

 
