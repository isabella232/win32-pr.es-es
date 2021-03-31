---
description: Los bloqueos oportunistas se solicitan abriendo primero un archivo con permisos y marcas adecuadas para la aplicación que abre el archivo. Todos los archivos para los que se solicitarán bloqueos oportunistas se deben abrir para una operación superpuesta (asincrónica).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Cómo solicitar un bloqueo oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912857"
---
# <a name="how-to-request-an-opportunistic-lock"></a>Cómo solicitar un bloqueo oportunista

Las aplicaciones cliente solo solicitan directamente bloqueos oportunistas cuando el bloqueo está diseñado para un archivo en el servidor local. Al tener acceso a los archivos de los servidores remotos, es el redirector de red, no la aplicación cliente, que solicita el bloqueo oportunista desde el servidor remoto.

Los bloqueos oportunistas se solicitan abriendo primero un archivo con permisos y marcas adecuadas para la aplicación que abre el archivo. Todos los archivos para los que se solicitarán bloqueos oportunistas se deben abrir para una operación superpuesta (asincrónica). Una vez abiertos los archivos para la operación superpuesta, utilice la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control adecuado para solicitar un bloqueo oportunista. Para obtener una lista de las operaciones de bloqueo oportunista, consulte [operaciones de bloqueo oportunista](opportunistic-lock-operations.md).

Las aplicaciones reciben una notificación de que se ha interrumpido un bloqueo oportunista mediante el miembro **hEvent** de la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada con el archivo. Las aplicaciones también pueden usar funciones como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) y [**HasOverlappedIoCompleted**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted). La aplicación es responsable de asociar el archivo correcto con el bloqueo oportunista roto.

Para obtener más información sobre las notificaciones, consulte [Synchronization](/windows/desktop/Sync/synchronization).

 

 
