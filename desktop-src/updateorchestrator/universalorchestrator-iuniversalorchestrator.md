---
title: Interfaz IUniversalOrchestrator
description: Una interfaz COM que proporciona métodos para permitir que un cliente se comunique con el orquestador universal.
ms.date: 01/14/2021
ms.topic: interface
ms.openlocfilehash: 6fa5dfd9f7853159645fbe3b543c228450f4e1c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/21/2021
ms.locfileid: "105720777"
---
# <a name="iuniversalorchestrator-interface"></a>Interfaz IUniversalOrchestrator

> [!NOTE] 
> Esta API pertenece a la API de orquestador universal.

**IUniversalOrchestrator** es una interfaz com que proporciona los métodos siguientes para permitir que un cliente se comunique con el orquestador universal.

## <a name="methods"></a>Métodos

|Método | Descripción |
|---|---|
|[:: Programar el programa](universalorchestrator-schedulework.md) | Registra el trabajo pendiente con el orquestador universal. |
|[::WorkCompleted](universalorchestrator-workcompleted.md) | Informa a la plataforma universal de que se ha completado todo el trabajo. |
|[::HasMoratoriumPassed](universalorchestrator-hasmoratoriumpassed.md) | Consulta a universal Orchestrator para determinar si funciona inmediatamente después de la nueva experiencia del dispositivo. |


## <a name="requirements"></a>Requisitos

| Requisito | Versión |
|---|---|
| Cliente mínimo compatible | Windows 10 1903 |
|   |   |