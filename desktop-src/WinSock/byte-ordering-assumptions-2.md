---
description: Estructuras sockaddr y suposiciones de ordenación de bytes en Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Suposiciones de ordenación de bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21c1e680b0fe658994723b0a1d87c2a7d6adbf0a00a5452b185401b03099089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097915"
---
# <a name="byte-ordering-assumptions"></a>Suposiciones de ordenación de bytes

Un proveedor de servicios debe tratar todos los componentes de [**sockaddr**](sockaddr-2.md) exclusivos del parámetro de familia de direcciones como si se encuentran en el orden de bytes de red y el parámetro de familia de direcciones como en el orden de bytes del equipo local. Es responsabilidad de la aplicación Winsock asegurarse de que las direcciones contenidas en las estructuras **de sockaddr** están organizadas correctamente. Winsock API proporciona una serie de rutinas de conversión para simplificar esta tarea. Actualmente, estas rutinas comprenden la conversión entre el orden de bytes natural del host local y el orden de bytes de red big-Endian o little-Endian. La arquitectura Winsock puede admitir otros esquemas de ordenación de bytes en el futuro.

 

 



