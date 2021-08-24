---
title: Errores de asignación de búfer RPC
description: Dado que la biblioteca en tiempo de ejecución de RPC asigna memoria para los búferes de envío y recepción, la función debe esperar errores de asignación de RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d68c484837f1f03bce8a8175ddb343065051e3695eec7c65d8a9de89c15fb5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745015"
---
# <a name="rpc-buffer-allocation-errors"></a>Errores de asignación de búfer RPC

Dado que la biblioteca en tiempo de ejecución de RPC asigna memoria para los búferes de envío y recepción, la función debe esperar errores de asignación de RPC. En caso de error de asignación de RPC, se invalida un identificador reanudable. Se trata de un requisito porque las funciones reanudables no se pueden rebobinar.

 

 




