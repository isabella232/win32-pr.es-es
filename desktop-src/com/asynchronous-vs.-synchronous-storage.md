---
title: Almacenamiento asincrónico y sincrónico
description: Almacenamiento asincrónico y sincrónico
ms.assetid: de8c50f8-1733-439f-ab53-f98ac21a1fae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884b8613bebf8ef401f76e4761f48fa0ddd831c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533544"
---
# <a name="asynchronous-and-synchronous-storage"></a>Almacenamiento asincrónico y sincrónico

Los monikers asincrónicos también pueden devolver un objeto de [almacenamiento asincrónico](/windows/desktop/Stg/asynchronous-storage) en la notificación [**IBindStatusCallback:: ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85)) . Este objeto de almacenamiento puede permitir el acceso a algunos de los datos persistentes del objeto mientras el enlace todavía está en curso. Un cliente puede elegir entre dos modos de almacenamiento: bloqueo y desbloqueo.

En el modo de bloqueo, que es compatible con las implementaciones actuales de los objetos de almacenamiento, si los datos no están disponibles, la llamada se bloquea hasta que llegan los datos. En el modo de no bloqueo, en lugar de bloquear la llamada, el objeto de almacenamiento devuelve un nuevo error E \_ pendiente cuando los datos no están disponibles. Un cliente que reconoce el enlace asincrónico y el almacenamiento anota este error y espera notificaciones adicionales ([**ondataavailable**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775061(v=vs.85))) para volver a intentar la operación. Un cliente puede elegir entre un almacenamiento sincrónico (bloqueo) y asincrónico (sin bloqueo) Si elige establecer la \_ marca BINDF ASYNCSTORAGE en el valor *grfBINDF* devuelto a [**IBindStatusCallback:: GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Monikers asincrónicos](asynchronous-monikers.md)
</dt> </dl>

 

 