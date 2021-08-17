---
title: Desarrollar un proveedor
description: Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API de seguimiento de eventos (ETW). Para obtener más información sobre cómo escribir un proveedor, vea Proporcionar eventos.
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bdcbf17113eb926aba245f270b84e7ab50bf3072e15a9a7752b8828296a00a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117937190"
---
# <a name="developing-a-provider"></a>Desarrollar un proveedor

Para escribir los eventos que defina en el manifiesto, use las funciones incluidas en la API [de seguimiento](/windows/desktop/ETW/event-tracing-portal) de eventos (ETW). Para obtener más información sobre cómo escribir un proveedor, vea [Proporcionar eventos](/windows/desktop/ETW/providing-events).

Después de escribir el proveedor, use la herramienta WevtUtil.exe para registrar el proveedor y el esquema. Para obtener más información sobre el uso de WevtUtil, [consulte Windows Event Log Tools](windows-event-log-tools.md). A continuación se muestra cómo usar WevtUtil para registrar un proveedor y quitar el registro.


```cmd
wevtutil im provider.man

wevtutil um provider.man
```