---
description: Los bloqueos oportunistas se solicitan abriendo primero un archivo con los permisos y marcas adecuados para que la aplicación abra el archivo. Todos los archivos para los que se van a solicitar bloqueos oportunistas deben abrirse para una operación superpuesta (asincrónica).
ms.assetid: a55d38c6-46e3-48e6-9b5b-d4f4234d8c07
title: Cómo solicitar un bloqueo oportunista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0dd6b99eb32ce191db78b55c4f8b79dafa340b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069929"
---
# <a name="how-to-request-an-opportunistic-lock"></a>Cómo solicitar un bloqueo oportunista

Las aplicaciones cliente solicitan directamente bloqueos oportunistas solo cuando el bloqueo está destinado a un archivo en el servidor local. Al acceder a archivos en servidores remotos, es el redirector de red, y no la aplicación cliente, el que solicita el bloqueo oportunista desde el servidor remoto.

Los bloqueos oportunistas se solicitan abriendo primero un archivo con los permisos y marcas adecuados para que la aplicación abra el archivo. Todos los archivos para los que se van a solicitar bloqueos oportunistas deben abrirse para una operación superpuesta (asincrónica). Una vez abiertos los archivos para la operación superpuesta, use la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con el código de control adecuado para solicitar un bloqueo oportunista. Para obtener una lista de las operaciones de bloqueo oportunista, vea [Operaciones de bloqueo oportunista.](opportunistic-lock-operations.md)

Se notifica a las aplicaciones que se ha roto un bloqueo oportunista mediante el **miembro hEvent** de la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) asociada al archivo. Las aplicaciones también pueden usar funciones como [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) [**y HasOverlappedIoCompleted.**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted) La aplicación es responsable de asociar el archivo correcto con el bloqueo oportunista roto.

Para obtener más información sobre la notificación, vea [Sincronización de](/windows/desktop/Sync/synchronization).

 

 
