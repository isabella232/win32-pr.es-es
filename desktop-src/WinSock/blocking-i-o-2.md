---
description: La forma más sencilla de e/s en Windows Sockets 2 es el bloqueo de e/s.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Bloqueo de entrada/salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696405"
---
# <a name="blocking-inputoutput"></a>Bloqueo de entrada/salida

La forma más sencilla de e/s en Windows Sockets 2 es el bloqueo de e/s. Como se mencionó en [modos y marcas de atributo de socket](socket-attribute-flags-and-modes-2.md), los sockets se crean de forma predeterminada en modo de bloqueo. Cualquier operación de e/s con un socket de bloqueo no volverá hasta que la operación se haya completado completamente. Por lo tanto, cualquier subproceso solo puede ejecutar una operación de e/s a la vez. Por ejemplo, si un subproceso emite una operación de recepción y no hay ningún dato disponible actualmente, el subproceso se bloqueará hasta que los datos estén disponibles y se coloquen en el búfer del subproceso. Aunque esto es sencillo, no es necesariamente la manera más eficaz de realizar operaciones de e/s (consulte [pseudo bloqueo y bloqueo real](pseudo-vs--true-blocking-2.md) para obtener más información).

 

 



