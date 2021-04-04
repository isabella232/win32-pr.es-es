---
description: Los recursos compartidos DDE son un recurso de equipo.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Recursos compartidos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910209"
---
# <a name="dde-shares"></a>Recursos compartidos DDE

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]

Los recursos compartidos DDE son un recurso de equipo. Son similares a los recursos compartidos de archivos porque se utilizan para controlar el acceso a un recurso. Con recursos compartidos de archivos, el recurso es un archivo. Con los recursos compartidos DDE, el recurso cambia de forma dinámica los datos. El tipo de datos intercambiados viene determinado por la aplicación de servidor que proporciona los datos y la aplicación cliente que solicita los datos.

El servidor llama a la función [**NDdeShareAdd**](nddeshareadd.md) para crear el recurso compartido DDE, que se almacena en el administrador de bases de datos de recursos compartidos DDE (DSDM).

El cliente inicia la conversación DDE conectándose al recurso compartido DDE. El cliente debe llamar a la función [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) para inicializar ddeml y llamar a la función [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) para conectarse al recurso compartido DDE. En la llamada a **DdeConnect** , el cliente especifica el nombre del servicio como se indica a continuación:

\\\\*Nombre del equipo* \\ NDDE $

donde *ComputerName* es el nombre del equipo que ejecuta la aplicación de servidor. NDDE $ indica que el tema proporcionado a [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) es el nombre del recurso compartido DDE en el equipo remoto denominado *NombreDeEquipo*.

Hay tres tipos de recursos compartidos DDE: antiguo, estilo nuevo y estático. Es habitual solo admitir el tipo estático. Los nombres de los recursos compartidos estáticos usan la Convención siguiente: *ShareName*$.

 

 
