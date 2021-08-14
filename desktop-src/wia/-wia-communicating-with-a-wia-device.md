---
description: Cuando un subproceso se comunica activamente con un dispositivo de adquisición de imágenes (WIA) de Windows (por ejemplo, transferencia de datos o escritura de propiedades del dispositivo), WIA &\# 0034; bloquea \#&0034; el dispositivo.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Comunicación con un dispositivo WIA en varios subprocesos o aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f54cc8fe9a3b60d684ff9a62def2c0cf8862576034b16f58d3dd369d2b8be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209269"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Comunicación con un dispositivo WIA en varios subprocesos o aplicaciones

Cuando un subproceso se comunica activamente con un dispositivo de adquisición de imágenes (WIA) de Windows (por ejemplo, transferencia de datos o escritura de propiedades del dispositivo), WIA "bloquea" el dispositivo. Cuando un dispositivo está bloqueado, ningún otro subproceso o proceso puede comunicarse activamente con ese dispositivo.

WIA no prohíbe que varios subprocesos o procesos mantengan conexiones a un único dispositivo. Es decir, un dispositivo solo se bloquea durante la comunicación real y dos o más aplicaciones pueden tener seleccionado simultáneamente un único dispositivo.

WIA crea un árbol de elementos independiente cada vez que cualquier subproceso o aplicación llama a [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md) para crear una instancia de ese dispositivo. WIA mantiene información de estado independiente para cada árbol de elementos. Por ejemplo, si un subproceso crea dos instancias de un analizador determinado, puede establecer diferentes resoluciones de examen para las dos instancias. Cuando se llama a [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) en una instancia determinada, WIA carga las propiedades asociadas a esa instancia en el dispositivo antes de que se lleve a cabo el examen real. Esto no afecta al estado de la otra instancia del dispositivo.

Si un subproceso tiene actualmente un dispositivo bloqueado (se está comunicando activamente con ese dispositivo) y otro subproceso intenta llamar a un método que se comunica activamente con el dispositivo, el método devuelve un error de WIA \_ ERROR \_ BUSY.

Normalmente, leer y escribir las propiedades del dispositivo tarda tan poco tiempo que estas operaciones rara vez provocan un conflicto. Sin embargo, la transferencia de datos normalmente tarda más tiempo y, por tanto, es más probable que cree conflictos de acceso a dispositivos. Es una programación sólida para evitar operaciones de dispositivos largas (transferencias de datos) simultáneamente en subprocesos independientes dentro de una aplicación.

Una aplicación nunca debe suponer que es la única aplicación que se comunica con un dispositivo WIA cuando se inicia.

 

 



