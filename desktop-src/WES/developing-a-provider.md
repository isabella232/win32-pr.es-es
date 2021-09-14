---
title: Desarrollar un proveedor
description: Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API de seguimiento de eventos (ETW). Para obtener más información sobre cómo escribir un proveedor, vea Proporcionar eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126885492"
---
# <a name="developing-a-provider"></a>Desarrollar un proveedor

Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API [de](/windows/desktop/ETW/event-tracing-portal) seguimiento de eventos (ETW). Para obtener más información sobre cómo escribir un proveedor, vea [Proporcionar eventos](/windows/desktop/ETW/providing-events).

Después de escribir el proveedor, use la herramienta WevtUtil.exe para registrar el proveedor y el esquema. Para obtener más información sobre el uso de WevtUtil, [consulte Windows Event Log Tools](windows-event-log-tools.md). A continuación se muestra cómo usar WevtUtil para registrar un proveedor y quitar el registro.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```