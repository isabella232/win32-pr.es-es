---
title: Interfaz IUniversalOrchestrator
description: Interfaz COM que proporciona métodos para permitir que un cliente se comunique con el orquestador universal.
ms.date: 01/14/2021
ms.topic: reference
ms.openlocfilehash: 5dbbaafb38ab9d790d32beca9b014f933d5d53d5
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991852"
---
# <a name="iuniversalorchestrator-interface"></a>Interfaz IUniversalOrchestrator

> [!NOTE] 
> Esta API pertenece a la API de Orquestador universal.

**IUniversalOrchestrator es** una interfaz COM que proporciona los métodos siguientes para permitir que un cliente se comunique con el Orquestador universal.

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