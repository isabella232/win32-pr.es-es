---
description: Sockaddr estructuras y suposiciones de orden de bytes en Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Suposiciones de orden de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705659"
---
# <a name="byte-ordering-assumptions"></a>Suposiciones de orden de bytes

Un proveedor de servicios debe tratar todos los componentes de [**sockaddr**](sockaddr-2.md) exclusivos del parámetro de la familia de direcciones como si estuvieran en el orden de bytes de la red, y el parámetro de la familia de direcciones como en el orden de bytes del equipo local. Es responsabilidad de la aplicación Winsock asegurarse de que las direcciones contenidas en las estructuras **sockaddr** están organizadas correctamente. La API de Winsock proporciona varias rutinas de conversión para simplificar esta tarea. Actualmente, estas rutinas comprenden la conversión entre el orden de bytes natural del host local y el orden de bytes de red big-endian o Little-Endian. La arquitectura de Winsock puede admitir otros esquemas de ordenación de bytes en el futuro.

 

 



