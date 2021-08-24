---
description: La separación de un bloqueo oportunista es el proceso de degradar el bloqueo que un cliente tiene en un archivo para que otro cliente pueda abrir el archivo, con o sin un bloqueo oportunista.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Separación de bloqueos oportunistas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b797feed06c5f02f1b87ff4e05e2d82d44a34f0efe86d7a0881ec1d722023f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582605"
---
# <a name="breaking-opportunistic-locks"></a>Separación de bloqueos oportunistas

La separación de un bloqueo oportunista es el proceso de degradar el bloqueo que un cliente tiene en un archivo para que otro cliente pueda abrir el archivo, con o sin un bloqueo oportunista. Cuando el otro cliente solicita la operación abierta, el servidor retrasa la operación de apertura y notifica al cliente que mantiene el bloqueo oportunista.

A continuación, el cliente que mantiene el bloqueo realiza las acciones adecuadas para el tipo de bloqueo, por ejemplo, abandonar los búferes de lectura, cerrar el archivo, y así sucesivamente. Solo cuando el cliente que contiene el bloqueo oportunista notifica al servidor que se ha hecho, el servidor abre el archivo para el cliente que solicita la operación de apertura. Sin embargo, cuando se bloquea un bloqueo de nivel 2, el servidor notifica al cliente que se ha roto, pero no espera ninguna confirmación, ya que no hay ningún dato almacenado en caché que se vacíe en el servidor.

Al confirmar una interrupción de cualquier bloqueo exclusivo (filtro, nivel 1 o lote), el titular de un bloqueo roto no puede solicitar otro bloqueo exclusivo. Puede degradar un bloqueo exclusivo a un bloqueo de nivel 2 o ningún bloqueo. El titular normalmente libera el bloqueo y cierra el archivo cuando está a punto de cerrar el archivo de todos modos.

Se notifica a las aplicaciones que se ha roto un bloqueo oportunista mediante el miembro **hEvent** de la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada al archivo en el que se ha roto el bloqueo. Las aplicaciones también pueden usar funciones como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) [**y HasOverlappedIoCompleted.**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)

 

 
