---
description: Cuando un subproceso se comunica activamente con un dispositivo de adquisición de imágenes de Windows (WIA) (por ejemplo, transfiriendo datos o escribiendo propiedades de dispositivo) WIA &\# 0034; bloquea&\# 0034; el dispositivo.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Comunicación con un dispositivo WIA en varios subprocesos o aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276861"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Comunicación con un dispositivo WIA en varios subprocesos o aplicaciones

Cuando un subproceso se comunica activamente con un dispositivo de adquisición de imágenes de Windows (WIA) (por ejemplo, mediante la transferencia de datos o la escritura de propiedades de dispositivo), WIA "bloquea" el dispositivo. Cuando un dispositivo está bloqueado, ningún otro subproceso o proceso puede comunicarse activamente con ese dispositivo.

WIA no prohíbe que varios subprocesos o procesos mantengan conexiones a un único dispositivo. Es decir, un dispositivo solo está bloqueado durante la comunicación real y dos o más aplicaciones pueden tener un único dispositivo seleccionado simultáneamente.

WIA crea un árbol de elementos independiente cada vez que cualquier subproceso o aplicación llama a [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md) para crear una instancia de ese dispositivo. WIA mantiene información de estado independiente para cada árbol de elementos. Por ejemplo, si un subproceso crea dos instancias de un escáner determinado, puede establecer diferentes resoluciones de digitalización para las dos instancias. Cuando se llama a [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) en una instancia determinada, WIA carga las propiedades asociadas a esa instancia en el dispositivo antes de que tenga lugar el examen real. Esto no afecta al estado de la otra instancia del dispositivo.

Si un subproceso tiene un dispositivo bloqueado actualmente (se comunica activamente con ese dispositivo) y otro subproceso intenta llamar a un método que se comunica activamente con el dispositivo, el método devuelve un \_ error de error de WIA \_ .

Normalmente, la lectura y la escritura de propiedades de dispositivo tardan tan poco tiempo en que estas operaciones causan un conflicto. La transferencia de datos, sin embargo, normalmente tarda más tiempo y, por lo tanto, es más probable que se creen conflictos de acceso a los dispositivos. Es una programación de sonido para evitar largas operaciones de dispositivo (transferencias de datos) simultáneamente en subprocesos independientes dentro de una aplicación.

Una aplicación nunca debe asumir que es la única aplicación que se comunica con un dispositivo WIA cuando se inicia.

 

 



