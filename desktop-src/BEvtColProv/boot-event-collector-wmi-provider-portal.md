---
description: El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración de la característica Recopilación de eventos de instalación y arranque en Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Proveedor WMI del recopilador de eventos de arranque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccebb4c4408aaa0ce58ad6ab412e4ca85fbb291c8da14ba764dfe3b19e2cbfa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579865"
---
# <a name="boot-event-collector-wmi-provider"></a>Proveedor WMI del recopilador de eventos de arranque

## <a name="purpose"></a>Propósito

El proveedor WMI del recopilador de eventos de arranque proporciona acceso a la información de conexión y configuración de la característica Recopilación de eventos de instalación y arranque en Windows Server. Esto le permite ver una lista de las conexiones actuales y el historial de conexiones entre un servidor recopilador y sus equipos de destino. Además, este proveedor permite administrar la configuración de un servidor recopilador.

> [!Note]  
> El proveedor WMI del recopilador de eventos de arranque se implementa en BEvtCol.exe.

 

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Recupera datos de reenvío de un equipo de destino.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Destinos conocidos que contienen los datos recopilados. Solo está disponible si el recopilador se está ejecutando con el registro de estado habilitado.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

Historial reciente de cambios en los datos de reenvío de un equipo de destino.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Control de la instancia del recopilador. Requiere los privilegios de administrador (BA).

</dd> </dl>

 

 



