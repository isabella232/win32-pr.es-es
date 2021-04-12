---
title: Errores de asignación de búfer de RPC
description: Dado que la biblioteca en tiempo de ejecución de RPC asigna memoria para los búferes de envío y recepción, la función debe esperar errores de asignación de RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357066"
---
# <a name="rpc-buffer-allocation-errors"></a>Errores de asignación de búfer de RPC

Dado que la biblioteca en tiempo de ejecución de RPC asigna memoria para los búferes de envío y recepción, la función debe esperar errores de asignación de RPC. En caso de un error de asignación de RPC, se invalida un identificador reanudable. Este es un requisito porque las funciones reanudables no se pueden rebobinar.

 

 




