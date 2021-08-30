---
title: E/S asincrónica y RPC asincrónica
description: La E/S asincrónica es un medio eficaz para que un único subproceso administre varias solicitudes de E/S simultáneamente.
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bdd198143c2f1f1d03aa73249680f47dec6d6ac6f996675df1f1e53fb56137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023815"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a>E/S asincrónica y RPC asincrónica

La E/S asincrónica es un medio eficaz para que un único subproceso administre varias solicitudes de E/S simultáneamente. RPC asincrónica en el servidor realiza un propósito similar para las solicitudes RPC. En versiones de Windows antes de Windows Vista, no se recomienda publicar solicitudes de E/S asincrónicas de procedimientos de servidor mediante RPC asincrónica. Sin embargo, en Windows Vista y versiones posteriores de Windows, las solicitudes de E/S asincrónicas asociadas a un puerto de finalización de E/S son compatibles con RPC asincrónico.

Antes de Windows Vista, una llamada a procedimiento remoto asincrónico puede completarse antes de que se complete la solicitud de E/S asincrónica. Cuando se completa la llamada asincrónica, su subproceso puede finalizar si el tiempo de ejecución de RPC decide que tiene suficientes subprocesos disponibles para dar servicio a la carga de trabajo esperada. El sistema enlaza todas las solicitudes de E/S al subproceso que las inicia. Si el subproceso finaliza, se anulan las solicitudes de E/S pendientes en ese subproceso. Las solicitudes de E/S pendientes no se pueden mover a otro subproceso.

Por lo tanto, los diseñadores de aplicaciones que tienen como destino versiones de Windows anteriores a Windows Vista pueden usar E/S sincrónica en procedimientos de servidor o pueden reenviar todas las solicitudes que implican E/S asincrónica a procedimientos que se ejecutan en un grupo de subprocesos que administra la aplicación. La API Windows proporciona funciones para la administración del grupo de subprocesos. Vea [Funciones de proceso y subproceso.](/windows/desktop/ProcThread/process-and-thread-functions)

 

 