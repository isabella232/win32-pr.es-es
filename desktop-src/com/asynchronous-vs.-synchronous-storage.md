---
title: Datos asincrónicos y sincrónicos Storage
description: Datos asincrónicos y sincrónicos Storage
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360878"
---
# <a name="asynchronous-and-synchronous-storage"></a>Datos asincrónicos y sincrónicos Storage

Los monikers asincrónicos también pueden devolver un objeto [Storage](/windows/desktop/Stg/asynchronous-storage) asincrónico en la [**notificación IBindStatusCallback::OnDataAvailable.**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) Este objeto de almacenamiento puede permitir el acceso a algunos de los datos persistentes del objeto mientras el enlace sigue en curso. Un cliente puede elegir entre dos modos para el almacenamiento: bloqueo y no bloqueo.

En el modo de bloqueo, que es compatible con las implementaciones actuales de objetos de almacenamiento, si los datos no están disponibles, la llamada se bloquea hasta que llegan los datos. En modo de no bloqueo, en lugar de bloquear la llamada, el objeto de almacenamiento devuelve un nuevo error E \_ PENDING cuando los datos no están disponibles. Un cliente que tenga en cuenta el enlace asincrónico y el almacenamiento anota este error y espera más notificaciones ([**OnDataAvailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) para reintentar la operación. Un cliente puede elegir entre un almacenamiento sincrónico (bloqueo) y asincrónico (sin bloqueo) si elige si se establece la marca BINDF ASYNCSTORAGE en el valor \_ *grfBINDF* devuelto a [**IBindStatusCallback::GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 