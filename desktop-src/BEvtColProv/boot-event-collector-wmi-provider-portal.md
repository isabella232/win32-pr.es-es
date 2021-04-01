---
description: El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración para la característica de recopilación de eventos de instalación y arranque en Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Proveedor WMI del recopilador de eventos de arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906946"
---
# <a name="boot-event-collector-wmi-provider"></a>Proveedor WMI del recopilador de eventos de arranque

## <a name="purpose"></a>Propósito

El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración para la característica de recopilación de eventos de instalación y arranque en Windows Server. Esto le permite ver una lista de las conexiones actuales y el historial de conexiones entre un servidor del recopilador y sus equipos de destino. Además, este proveedor le permite administrar la configuración de un servidor de recopilador.

> [!Note]  
> El proveedor WMI del recopilador de eventos de arranque se implementa en BEvtCol.exe.

 

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Recupera los datos de reenvío de un equipo de destino.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Destinos conocidos que contienen los datos recopilados. Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

El historial reciente de cambios en los datos de reenvío para un equipo de destino.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Control de la instancia del recopilador. Requiere los privilegios de administrador (BA).

</dd> </dl>

 

 



