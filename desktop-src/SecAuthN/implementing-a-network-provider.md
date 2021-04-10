---
description: Un proveedor de red es un archivo DLL que permite que el sistema operativo Windows admita un protocolo de red específico.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementación de un proveedor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97819b033c57feb25cf882f97051785123e2e382
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153841"
---
# <a name="implementing-a-network-provider"></a>Implementación de un proveedor de red

Un proveedor de red es un archivo DLL que permite que el sistema operativo Windows admita un protocolo de red específico. Para ello, implementa la API del proveedor de red. Esta API es un conjunto de funciones a las que el [*enrutador de varios proveedores*](../secgloss/m-gly.md) (MPR) llama para comunicarse con la red. A continuación, el proveedor de red traduce estas llamadas a llamadas API específicas de la red para realizar la acción especificada por el MPR. De esta manera, el sistema operativo Windows puede interactuar con nuevos protocolos de red sin tener que entender las API específicas de la red.

Para crear un proveedor de red, escriba un archivo DLL que exporte la función [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) .

La compatibilidad con las demás funciones de la API del proveedor de red es opcional. Si el proveedor de red no requiere una función, el archivo DLL no necesita implementarlo ni proporcionar una implementación de código auxiliar. Para obtener más información, vea los temas de función individual en [funciones de proveedor de red](authentication-functions.md).

La excepción es que si admite una de las siguientes funciones de enumeración, debe admitir también las otras dos funciones: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)y [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

Las instrucciones siguientes describen cómo escribir un proveedor de red que interactúe bien con el MPR y el sistema operativo Windows. Siempre que sea posible, el proveedor debe cumplir las siguientes directrices para la velocidad, la validación y el enrutamiento.

## <a name="speed"></a>Velocidad

Un proveedor de red debe determinar rápidamente si un recurso de red es el suyo propio. Esto se debe a que es posible que el MPR tenga que recorrer muchos proveedores para encontrar el propietario de un recurso.

Si el proveedor de red no posee el recurso, debe devolver de inmediato el código de estado de red de red incorrecta de WN \_ \_ .

También es importante que los proveedores que admiten [**NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) devuelvan los resultados de esta función rápidamente porque se llama mientras WinFile está pintando el árbol de directorios.

## <a name="validation"></a>Validación

El orden de validación es importante. Un proveedor de red debe determinar primero si se ha iniciado su red y, a continuación, determinar si la red y el proveedor de red admiten la operación. Si, después de estas comprobaciones, el proveedor de red recibe los recursos de red, debe determinar si es propietario de ellos. Por último, debe validar otros parámetros.

## <a name="routing"></a>Enrutamiento

Si el MPR tiene que recorrer los proveedores de red, probará todos los proveedores hasta que uno acepte la llamada. En otras palabras, el MPR siempre continúa intentando encontrar un proveedor de red.

Sin embargo, toma nota del primer error significativo informado por un proveedor. Errores como ERROR \_ NETPATH erróneo \_ , error de \_ \_ nombre de red, error de \_ \_ parámetro no válido. el nivel de \_ error \_ no válido \_ se considera insignificante porque simplemente significa que el proveedor no administra el recurso. Sin embargo, si se produce un error en el proveedor con el error \_ contraseña no válida \_ o algún otro error significativo, MPR registra este error y continúa el ciclo de los proveedores de red. En general, cuando se realiza el enrutamiento, si ningún proveedor acepta la llamada, el MPR informa del primer error significativo que encuentra al recorrer los proveedores de red.

El proveedor de red debe tener en cuenta este comportamiento del MPR al decidir qué mensaje de error devolver.

## <a name="implementation-note"></a>Nota de implementación

Al implementar las DLL de proveedor de red, el proveedor no debe llamar a otras [funciones de red de Windows](../wnet/windows-networking-functions.md), API de [Shell](../shell/samples-usingthumbnailproviders.md)u otras consultas basadas en rutas de acceso UNC que podrían provocar la reentrada en el subsistema de mpr. Si realiza este tipo de llamadas desde una DLL de proveedor de red, la aplicación u otros componentes del sistema operativo pueden experimentar contención, un bajo rendimiento o interbloqueos dentro del subsistema de MPR.

 

 
