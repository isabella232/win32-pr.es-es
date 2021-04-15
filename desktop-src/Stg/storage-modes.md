---
title: Modos de almacenamiento
description: El almacenamiento asincrónico admite dos modos de almacenamiento que bloquean y no bloquean, que un cliente (ya sea un explorador o el propio objeto) puede especificar devolviendo BINDF \_ ASYNCSTORAGE desde la llamada del moniker a IBindStatusCallback GetBindInfo.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827e893f5077a64485251111837e6b56657756f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421131"
---
# <a name="storage-modes"></a>Modos de almacenamiento

El almacenamiento asincrónico admite dos modos de almacenamiento: bloqueo y desbloqueo, que un cliente (ya sea un explorador o el propio objeto) puede especificar devolviendo BINDF \_ ASYNCSTORAGE desde la llamada del moniker a [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)). Si un cliente especifica BINDF \_ ASYNCSTORAGE, recibe un puntero a un almacenamiento asincrónico sin bloqueos. De lo contrario, recibe un puntero a un almacenamiento asincrónico de bloqueo. Aunque el cliente no solicite una operación de enlace asincrónica (al no registrar [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con el contexto de enlace), el moniker sigue devolverá un almacenamiento asincrónico de bloqueo, lo que permite la carga progresiva de las aplicaciones heredadas.

En el modo de no bloqueo, un almacenamiento asincrónico devuelve E \_ pendiente cuando los datos no están disponibles. Al recibir este mensaje, el cliente espera la notificación de que hay datos adicionales disponibles antes de intentar descargarlo de nuevo.

En el modo de bloqueo, en lugar de devolver E \_ pendiente, el almacenamiento asincrónico bloquea la llamada hasta que los nuevos datos estén disponibles y, a continuación, desbloquea la llamada y devuelve los nuevos datos. El cliente debe estar listo para recibir los datos. Mientras se bloquea el subproceso, los datos que ya se han pasado al cliente están totalmente disponibles para el usuario.

El modo de bloqueo es necesario porque los clientes que no reconocen el almacenamiento asincrónico no reconocerán E \_ pendientes y asumirán que se ha producido un error irrecuperable. El bloqueo del almacenamiento asincrónico permite que los clientes existentes realicen una representación progresiva.

 

 