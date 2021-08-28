---
description: A veces es necesario reemplazar un archivo DLL por una versión más reciente.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Dynamic-Link de biblioteca de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f294e16efac60da843c14d200aaa768d4fc78ce8a922cb0aa6958756a9903be0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075545"
---
# <a name="dynamic-link-library-updates"></a>Dynamic-Link de biblioteca de aplicaciones

A veces es necesario reemplazar un archivo DLL por una versión más reciente. Antes de reemplazar un archivo DLL, realice una comprobación de versión para asegurarse de que va a reemplazar una versión anterior por una versión más reciente. Es posible reemplazar un archivo DLL que esté en uso. El método que se usa para reemplazar los archivos DLL que están en uso depende del sistema operativo que use. En Windows XP y versiones posteriores, las aplicaciones deben usar aplicaciones aisladas y [ensamblados en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

No es necesario reiniciar el equipo si realiza los pasos siguientes:

1.  Use la [**función MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) para cambiar el nombre del archivo DLL que se va a reemplazar. No especifique MOVEFILE COPY ALLOWED y asegúrese de que el archivo cuyo nombre ha cambiado se encuentra en el \_ mismo volumen que contiene el archivo \_ original. También puede cambiar el nombre del archivo en el mismo directorio si le proporciona una extensión diferente.
2.  Copie el nuevo archivo DLL en el directorio que contiene el archivo DLL cuyo nombre ha cambiado. Todas las aplicaciones ahora usarán el nuevo archivo DLL.
3.  Use [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con MOVEFILE \_ DELAY UNTIL REBOOT para eliminar el archivo DLL cuyo nombre ha \_ \_ cambiado.

Antes de realizar este reemplazo, las aplicaciones usarán el archivo DLL original hasta que se descargue. Después de realizar el reemplazo, las aplicaciones usarán el nuevo archivo DLL. Al escribir un archivo DLL, debe tener cuidado de asegurarse de que está preparado para esta situación, especialmente si el archivo DLL mantiene información de estado global o se comunica con otros servicios. Si el archivo DLL no está preparado para un cambio en la información de estado global o los protocolos de comunicación, la actualización del archivo DLL requerirá reiniciar el equipo para asegurarse de que todas las aplicaciones usan la misma versión del archivo DLL.

 

 
