---
description: WMI utiliza el seguimiento de eventos (ETW) y los eventos se pueden obtener a través de la interfaz de usuario Visor de eventos o la herramienta de línea de comandos wevtutil. Para obtener más información, vea seguimiento de la actividad WMI.
ms.assetid: 315b8355-03b9-40f9-a6c1-29a49f5a2cd8
ms.tgt_platform: multiple
title: Archivos de registro de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51dfe4efbec32e60812980511676f723fd5aee9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696781"
---
# <a name="wmi-log-files"></a>Archivos de registro de WMI

WMI utiliza el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW) y los eventos se pueden obtener a través de la interfaz de usuario **visor de eventos** o la herramienta de línea de comandos wevtutil. Para obtener más información, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md).

-   [Seguimiento de eventos en lugar de registros de texto](#event-tracing-instead-of-text-logs)
-   [Archivos de registro de WMI](#wmi-log-files)
-   [Temas relacionados](#related-topics)

## <a name="event-tracing-instead-of-text-logs"></a>Seguimiento de eventos en lugar de registros de texto

La actividad del servicio WMI se registra en el archivo WMITracing. log. Para obtener más información sobre la habilitación del seguimiento de eventos WMI y el acceso al archivo WMITracing. log, vea seguimiento de la [actividad WMI](tracing-wmi-activity.md). Los proveedores Modelo de controlador de Windows (WDM) continúan registrando en el archivo Wbemprov. log.

## <a name="wmi-log-files"></a>Archivos de registro de WMI

El servicio WMI y algunos proveedores escriben archivos de registro de texto en los eventos de registro.

<dl> <dt>

<span id="WMI_Provider_Log_Files"></span><span id="wmi_provider_log_files"></span><span id="WMI_PROVIDER_LOG_FILES"></span>[Archivos de registro del proveedor WMI](wmi-provider-log-files.md)
</dt> <dd>

Los proveedores WMI también pueden mantener registros. Los archivos de registro que aparecen en un sistema dependen de los proveedores instalados.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de WMI](wmi-reference.md)
</dt> <dt>

[Seguimiento de la actividad WMI](tracing-wmi-activity.md)
</dt> <dt>

[Registrar la actividad WMI](logging-wmi-activity.md)
</dt> </dl>

 

 
