---
title: Desarrollo de un proveedor
description: Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API de seguimiento de eventos (ETW). Para obtener más información sobre cómo escribir un proveedor, consulte proporcionar eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149556"
---
# <a name="developing-a-provider"></a>Desarrollo de un proveedor

Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API de [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW). Para obtener más información sobre cómo escribir un proveedor, consulte [proporcionar eventos](/windows/desktop/ETW/providing-events).

Después de escribir el proveedor, utilice la herramienta WevtUtil.exe para registrar el proveedor y el esquema. Para más información sobre el uso de WevtUtil, consulte [herramientas de registro de eventos de Windows](windows-event-log-tools.md). A continuación se muestra cómo usar WevtUtil para registrar un proveedor y para quitar el registro.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```