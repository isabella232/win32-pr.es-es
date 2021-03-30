---
description: A veces es necesario reemplazar un archivo DLL por una versión más reciente.
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Actualizaciones de la biblioteca Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f76103ddebc723466fb7e32a216c0c039691d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082287"
---
# <a name="dynamic-link-library-updates"></a>Actualizaciones de la biblioteca Dynamic-Link

A veces es necesario reemplazar un archivo DLL por una versión más reciente. Antes de reemplazar un archivo DLL, realice una comprobación de la versión para asegurarse de que está reemplazando una versión anterior por una versión más reciente. Es posible reemplazar un archivo DLL que esté en uso. El método que se utiliza para reemplazar los archivos DLL que se están usando depende del sistema operativo que se use. En Windows XP y versiones posteriores, las aplicaciones deben usar [aplicaciones aisladas y ensamblados en paralelo](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

No es necesario reiniciar el equipo si realiza los siguientes pasos:

1.  Utilice la función [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) para cambiar el nombre del archivo DLL que se va a reemplazar. No especifique la \_ copia MOVEFILE \_ permitida y asegúrese de que el archivo al que se ha cambiado el nombre está en el mismo volumen que contiene el archivo original. También puede cambiar simplemente el nombre del archivo en el mismo directorio asignándole una extensión diferente.
2.  Copie el nuevo archivo DLL en el directorio que contiene el archivo DLL al que se ha cambiado el nombre. Todas las aplicaciones usarán ahora el nuevo archivo DLL.
3.  Use [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) con \_ el retraso de MOVEFILE \_ hasta que \_ se reinicie para eliminar el archivo dll al que se ha cambiado el nombre.

Antes de hacer este reemplazo, las aplicaciones usarán el archivo DLL original hasta que se descargue. Después de hacer el reemplazo, las aplicaciones usarán el nuevo archivo DLL. Al escribir un archivo DLL, debe asegurarse de que está preparado para esta situación, especialmente si el archivo DLL mantiene información de estado global o se comunica con otros servicios. Si la DLL no está preparada para un cambio en la información de estado global o en los protocolos de comunicación, la actualización de la DLL requerirá que reinicie el equipo para asegurarse de que todas las aplicaciones usen la misma versión del archivo DLL.

 

 
