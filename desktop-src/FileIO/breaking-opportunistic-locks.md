---
description: Interrumpir un bloqueo oportunista es el proceso de degradar el bloqueo que un cliente tiene en un archivo para que otro cliente pueda abrir el archivo, con o sin un bloqueo oportunista.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Interrumpir bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669700"
---
# <a name="breaking-opportunistic-locks"></a>Interrumpir bloqueos oportunistas

Interrumpir un bloqueo oportunista es el proceso de degradar el bloqueo que un cliente tiene en un archivo para que otro cliente pueda abrir el archivo, con o sin un bloqueo oportunista. Cuando el otro cliente solicita la operación de apertura, el servidor retrasa la operación de apertura y notifica al cliente que contiene el bloqueo oportunista.

El cliente que mantiene el bloqueo toma las medidas adecuadas para el tipo de bloqueo, por ejemplo, el abandono de los búferes de lectura, el cierre del archivo, etc. Solo cuando el cliente que contiene el bloqueo oportunista notifica al servidor que se ha hecho, el servidor abre el archivo para el cliente que solicita la operación de apertura. Sin embargo, cuando se interrumpe un bloqueo de nivel 2, el servidor informa al cliente de que se ha interrumpido pero no espera ninguna confirmación, ya que no hay ningún dato en caché que se vacíe en el servidor.

En la confirmación de una interrupción de un bloqueo exclusivo (filtro, nivel 1 o lote), el titular de un bloqueo roto no puede solicitar otro bloqueo exclusivo. Puede degradar un bloqueo exclusivo a un bloqueo de nivel 2 o no tener ningún bloqueo. Normalmente, el titular libera el bloqueo y cierra el archivo cuando está a punto de cerrar el archivo de todos modos.

Las aplicaciones reciben una notificación de que se ha interrumpido un bloqueo oportunista mediante el miembro **hEvent** de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada al archivo en el que se ha interrumpido el bloqueo. Las aplicaciones también pueden usar funciones como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) y [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted).

 

 
