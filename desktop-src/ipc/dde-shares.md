---
description: Los recursos compartidos DDE son un recurso de máquina.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Recursos compartidos de DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e3416235f78e48c68b7d2e35c7ac042f8ff5d6eac79cc2471efa5ea12d82b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602125"
---
# <a name="dde-shares"></a>Recursos compartidos de DDE

\[Ya no se admite DDE de red. Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ NOT \_ IMPLEMENTED.\]

Los recursos compartidos DDE son un recurso de máquina. Son similares a los recursos compartidos de archivos porque se usan para controlar el acceso a un recurso. Con los recursos compartidos de archivos, el recurso es un archivo. Con los recursos compartidos de DDE, el recurso se intercambia dinámicamente de datos. El tipo de datos intercambiados viene determinado por la aplicación de servidor que proporciona los datos y la aplicación cliente que solicita los datos.

El servidor llama a la [**función NDdeShareAdd**](nddeshareadd.md) para crear el recurso compartido DDE, que se almacena en el Administrador de bases de datos de recursos compartidos de DDE (DSDM).

El cliente inicia la conversación de DDE conectándose al recurso compartido de DDE. El cliente debe llamar a la función [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) para inicializar DDEML y llamar a la función [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) para conectarse al recurso compartido de DDE. En la **llamada a DdeConnect,** el cliente especifica el nombre del servicio de la manera siguiente:

\\\\*NombreDeEquipo* \\ NDDE$

donde *ComputerName* es el nombre del equipo que ejecuta la aplicación de servidor. NDDE$ indica que el tema proporcionado a [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) es el nombre del recurso compartido de DDE en el equipo remoto denominado *NombreDeEquipo*.

Hay tres tipos de recursos compartidos de DDE: estilo antiguo, estilo nuevo y estático. Es habitual admitir solo el tipo estático. Los nombres de los recursos compartidos estáticos usan la convención siguiente: *ShareName*$.

 

 
