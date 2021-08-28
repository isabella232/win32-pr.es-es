---
title: Interfaz IUniversalOrchestrator
description: Interfaz COM que proporciona métodos para permitir que un cliente se comunique con el orquestador universal.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: f3635f76236eb6c7a11bfa62311003b7d76357a9fbacc9fde85f0bdffed0c129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966144"
---
# <a name="iuniversalorchestrator-interface"></a>Interfaz IUniversalOrchestrator

> [!NOTE] 
> Esta API pertenece a la API de Orquestador universal.

**IUniversalOrchestrator** es una interfaz COM que proporciona los métodos siguientes para permitir que un cliente se comunique con el orquestador universal.

## <a name="methods"></a>Métodos

|Método | Descripción |
|---|---|
|[::ScheduleWork](universalorchestrator-schedulework.md) | Registra el trabajo pendiente con el orquestador universal. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informa al orquestador universal de que todo el trabajo ha finalizado. |
|[::HasMofiliaPassed](universalorchestrator-hasmoratoriumpassed.md) | Consulta a Universal Orchestrator para determinar si funciona inmediatamente después de la nueva experiencia de configuración de dispositivo. |


## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |