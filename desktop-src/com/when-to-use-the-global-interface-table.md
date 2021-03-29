---
title: Cuándo usar la tabla de interfaz global
description: Cuándo usar la tabla de interfaz global
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078413"
---
# <a name="when-to-use-the-global-interface-table"></a>Cuándo usar la tabla de interfaz global

Si va a calcular las referencias de un puntero de interfaz varias veces entre apartamentos en un proceso, puede usar la interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Con otras técnicas, tendría que volver a calcular las referencias de cada vez.

> [!Note]  
> Si el puntero de interfaz no se calcula una sola vez, puede que desee usar la función [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) . También se puede usar para pasar un puntero de interfaz de un subproceso a otro subproceso en el mismo proceso.

 

La interfaz [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) también hace que otro problema con anterioridad difícil sea más sencillo para el programador. Este problema se produce cuando se cumplen las condiciones siguientes:

-   Un objeto ágil en proceso agrega el contador de referencias de subprocesamiento libre.
-   Este mismo objeto ágil también contiene punteros de interfaz (como variables de miembro) a otros objetos que no son ágiles y no agregan el contador de referencias de subprocesamiento libre.

En esta situación, si el objeto externo obtiene las referencias a otro apartamento y la aplicación llama a en él, y el objeto intenta llamar a en cualquiera de sus punteros de interfaz de variable miembro que no son de subprocesamiento libre o que son proxies a objetos de otros apartamentos, podría obtener resultados incorrectos o el \_ subproceso RPC E incorrecto de error \_ \_ . Este error se produce porque la interfaz interna está diseñada para que solo se pueda llamar desde el apartamento en el que se almacenó por primera vez en la variable miembro.

Para solucionar este problema, el objeto externo que agrega el contador de referencias de subprocesamiento libre debe llamar a [**IGlobalInterfaceTable:: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) en la interfaz interna y almacenar la cookie resultante en su variable miembro, en lugar de almacenar el puntero de interfaz real. Cuando el objeto externo desea llamar a en el puntero de interfaz de un objeto interno, debe llamar a [**IGlobalInterfaceTable:: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), usar el puntero de interfaz devuelto y, a continuación, liberarlo. Cuando el objeto externo desaparece, debe llamar a [**IGlobalInterfaceTable:: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) para quitar la interfaz de la tabla de interfaz global.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear la tabla de interfaz global](creating-the-global-interface-table.md)
</dt> </dl>

 

 