---
description: La forma más sencilla de E/S en Windows Sockets 2 es bloquear la E/S.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Entrada/salida de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c65991f4401a5069718fb39172a9d59db4536a83ab4e2f99948d7c300eb4042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322619"
---
# <a name="blocking-inputoutput"></a>Entrada/salida de bloqueo

La forma más sencilla de E/S en Windows Sockets 2 es bloquear la E/S. Como se mencionó en [Socket Attribute Flags and Modes](socket-attribute-flags-and-modes-2.md)(Marcas y modos de atributo de socket), los sockets se crean en modo de bloqueo de forma predeterminada. Las operaciones de E/S con un socket de bloqueo no se devolverán hasta que la operación se haya completado por completo. Por lo tanto, cualquier subproceso solo puede ejecutar una operación de E/S a la vez. Por ejemplo, si un subproceso emite una operación de recepción y no hay datos disponibles actualmente, el subproceso se bloqueará hasta que los datos estén disponibles y se coloquen en el búfer del subproceso. Aunque esto es sencillo, no es necesariamente la manera más eficaz de realizar E/S (consulte Pseudo blocking and True Blocking (Pseudo [blocking y true blocking)](pseudo-vs--true-blocking-2.md) para obtener más información).

 

 



