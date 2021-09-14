---
title: Storage Modos
description: El almacenamiento asincrónico admite dos modos de bloqueo y no bloqueo de almacenamiento, que un cliente (ya sea un explorador o el propio objeto) puede especificar devolviendo BINDF ASYNCSTORAGE desde la llamada del \_ moniker a IBindStatusCallback GetBindInfo.
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827e893f5077a64485251111837e6b56657756f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073540"
---
# <a name="storage-modes"></a>Storage Modos

El almacenamiento asincrónico admite dos modos de almacenamiento: bloqueo y no bloqueo, que un cliente (ya sea un explorador o el propio objeto) puede especificar devolviendo BINDF ASYNCSTORAGE desde la llamada del \_ moniker a [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)). Si un cliente especifica BINDF \_ ASYNCSTORAGE, recibe un puntero a un almacenamiento asincrónico sin bloqueo. De lo contrario, recibe un puntero a un almacenamiento asincrónico de bloqueo. Incluso si el cliente no solicita una operación de enlace asincrónica (al no registrar [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) con el contexto de enlace), el moniker sigue devuelve un almacenamiento asincrónico de bloqueo, lo que habilita la carga progresiva para las aplicaciones heredadas.

En el modo de no bloqueo, un almacenamiento asincrónico devuelve E \_ PENDING cuando los datos no están disponibles. Al recibir este mensaje, el cliente espera la notificación de que hay datos adicionales disponibles antes de intentar descargarlos de nuevo.

En modo de bloqueo, en lugar de devolver E PENDING, el almacenamiento asincrónico bloquea la llamada hasta que haya nuevos datos disponibles y, a continuación, desbloquea la llamada y \_ devuelve los nuevos datos. El cliente debe estar listo para recibir los datos. Mientras el subproceso está bloqueado, los datos que ya se han pasado al cliente están totalmente disponibles para el usuario.

El modo de bloqueo es necesario porque los clientes que no son conscientes del almacenamiento asincrónico no reconocerán E PENDING y asumirán que se ha producido \_ un error irrecuperable. El bloqueo del almacenamiento asincrónico permite a los clientes existentes realizar una representación progresiva.

 

 