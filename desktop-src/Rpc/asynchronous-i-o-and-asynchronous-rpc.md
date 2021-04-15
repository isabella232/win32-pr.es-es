---
title: RPC asincrónica y de e/s asincrónica
description: La e/s asincrónica es un medio eficaz para que un único subproceso administre varias solicitudes de e/s simultáneamente.
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932e85283eb67ff6675a646e791bbce5fe15d65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421292"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a>RPC asincrónica y de e/s asincrónica

La e/s asincrónica es un medio eficaz para que un único subproceso administre varias solicitudes de e/s simultáneamente. RPC asincrónico en el servidor lleva a cabo un propósito similar para las solicitudes RPC. En las versiones de Windows anteriores a Windows Vista, no se recomienda el envío de solicitudes de e/s asincrónicas desde procedimientos de servidor mediante RPC asincrónico. Sin embargo, en Windows Vista y versiones posteriores de Windows, las solicitudes de e/s asincrónicas que están asociadas a un puerto de finalización de e/s son compatibles con RPC asincrónico.

Antes de Windows Vista, una llamada a procedimiento remoto asincrónica puede completarse antes de que se complete la solicitud de e/s asincrónica. Cuando se completa la llamada asincrónica, su subproceso puede terminar si el tiempo de ejecución de RPC decide que tiene suficientes subprocesos disponibles para dar servicio a la carga de trabajo esperada. El sistema enlaza todas las solicitudes de e/s al subproceso que las inicia. Si el subproceso finaliza, se anulan las solicitudes de e/s pendientes en ese subproceso. Las solicitudes de e/s pendientes no se pueden pasar a otro subproceso.

Por lo tanto, los diseñadores de aplicaciones que tienen como destino versiones de Windows anteriores a Windows Vista pueden usar e/s sincrónicas en los procedimientos de servidor, o pueden reenviar todas las solicitudes que impliquen la e/s asincrónica a los procedimientos que se ejecutan en un grupo de subprocesos que administra la aplicación. La API de Windows proporciona funciones para la administración de grupos de subprocesos. Consulte [funciones de proceso y subproceso](/windows/desktop/ProcThread/process-and-thread-functions).

 

 