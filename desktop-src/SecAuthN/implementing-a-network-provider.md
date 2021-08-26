---
description: Un proveedor de red es un archivo DLL que permite al Windows operativo admitir un protocolo de red específico.
ms.assetid: 21dfa941-72fd-4f2c-8bc4-379ed6ca2a4c
title: Implementar un proveedor de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4776bd97b9528bd04bbda25b88e0ff45a8f911429bb573e62dbbb8581abdfbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015985"
---
# <a name="implementing-a-network-provider"></a>Implementar un proveedor de red

Un proveedor de red es un archivo DLL que permite al Windows operativo admitir un protocolo de red específico. Para ello, implementa la API del proveedor de red. Esta API es un conjunto de funciones a las que [*llama el*](../secgloss/m-gly.md) enrutador de varios proveedores (MPR) para comunicarse con la red. A continuación, el proveedor de red convierte estas llamadas en llamadas API específicas de la red para realizar la acción especificada por el MPR. De esta manera, el Windows operativo puede interactuar con nuevos protocolos de red sin tener que comprender sus API específicas de la red.

Para crear un proveedor de red, escriba un archivo DLL que exporte la [**función NPGetCaps.**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)

La compatibilidad con las demás funciones de la API del proveedor de red es opcional. Si el proveedor de red no requiere una función, el archivo DLL no necesita implementarla ni proporcionar una implementación de código auxiliar. Para obtener más información, vea los temas de funciones individuales en [Funciones del proveedor de red](authentication-functions.md).

La excepción es que si admite una de las siguientes funciones de enumeración, también debe admitir las otras dos funciones: [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)y [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum).

En las siguientes directrices se describe cómo escribir un proveedor de red que interactúe bien con el MPR y el Windows operativo. Siempre que sea posible, el proveedor debe cumplir las siguientes directrices de velocidad, validación y enrutamiento.

## <a name="speed"></a>Velocidad

Un proveedor de red debe determinar rápidamente si un recurso de red es propio. Esto se debe a que mpr puede tener que recorrer varios proveedores para encontrar al propietario de un recurso.

Si el proveedor de red no es el propietario del recurso, debe devolver inmediatamente el código de estado DE \_ \_ NETNAME BAD de WN.

También es importante que los proveedores que [**admiten NPGetDirectoryType**](/windows/desktop/api/Npapi/nf-npapi-npgetdirectorytype) devuelvan resultados para esta función rápidamente porque se llama mientras WinFile pinta el árbol de directorios.

## <a name="validation"></a>Validación

El orden de validación es importante. En primer lugar, un proveedor de red debe determinar si su red se ha iniciado y, a continuación, determinar si la red y el proveedor de red admiten la operación. Si, después de estas comprobaciones, el proveedor de red recibe recursos de red, debe determinar si los posee. Por último, debe validar otros parámetros.

## <a name="routing"></a>Enrutamiento

Si MPR tiene que recorrer en ciclo los proveedores de red, probará todos los proveedores hasta que uno acepte la llamada. En otras palabras, MPR siempre sigue intentando encontrar un proveedor de red.

Sin embargo, toma nota del primer error significativo notificado por un proveedor. Errores como ERROR \_ BAD \_ NETPATH, ERROR \_ BAD NET \_ \_ NAME, ERROR INVALID \_ PARAMETER, ERROR INVALID \_ \_ \_ LEVEL se consideran insignificantes porque simplemente significan que el proveedor no administra el recurso. Sin embargo, si se produce un error en el proveedor con el error ERROR INVALID PASSWORD u otro error significativo, MPR registra este error y continúa el ciclo a través de \_ \_ los proveedores de red. En general, al enrutar, si ningún proveedor acepta la llamada, el MPR notifica el primer error significativo que encuentra al atravesar los proveedores de red.

El proveedor de red debe tener en cuenta este comportamiento de MPR al decidir qué mensaje de error devolver.

## <a name="implementation-note"></a>Nota de implementación

Al implementar dll de proveedor de red, el proveedor no debe llamar a otras funciones de red de [Windows,](../wnet/windows-networking-functions.md)API de [shell](../shell/samples-usingthumbnailproviders.md)u otras consultas basadas en rutas de acceso UNC que podrían provocar la reentrada en el subsistema MPR. Si realiza estas llamadas desde un archivo DLL del proveedor de red, la aplicación u otros componentes del sistema operativo pueden experimentar contención, un rendimiento deficiente o interbloqueos dentro del subsistema MPR.

 

 
