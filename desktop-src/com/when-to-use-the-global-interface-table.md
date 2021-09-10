---
title: Cuándo usar la tabla de interfaz global
description: Cuándo usar la tabla de interfaz global
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369495"
---
# <a name="when-to-use-the-global-interface-table"></a>Cuándo usar la tabla de interfaz global

Si va a desmarque un puntero de interfaz varias veces entre los departamentos de un proceso, puede usar la [**interfaz IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Con otras técnicas, tendría que volver a casarse cada vez.

> [!Note]  
> Si el puntero de interfaz se desmarque solo una vez, puede que desee usar la [**función CoMarshalInterThreadInterfaceInStream.**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) También se puede usar para pasar un puntero de interfaz de un subproceso a otro subproceso en el mismo proceso.

 

La [**interfaz IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) también simplifica otro problema anteriormente difícil para el programador. Este problema se produce cuando se aplican las condiciones siguientes:

-   Un objeto agile en proceso agrega el serializador de subproceso libre.
-   Este mismo objeto ágil también contiene (como variables miembro) punteros de interfaz a otros objetos que no son ágiles y no agregan el serializador de subproceso libre.

En esta situación, si el objeto externo se serializa en otro apartamento y la aplicación llama a él, y el objeto intenta llamar a en cualquiera de sus punteros de interfaz de variable miembro que no son subprocesos libres o son servidores proxy a objetos de otros departamentos, podría obtener resultados incorrectos o el error RPC \_ E \_ WRONG \_ THREAD. Este error se produce porque la interfaz interna está diseñada para que solo se pueda llamar desde el apartamento en el que se almacenaba por primera vez en la variable miembro.

Para resolver este problema, el objeto externo que agrega el serializador de subproceso libre debe llamar a [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) en la interfaz interna y almacenar la cookie resultante en su variable miembro, en lugar de almacenar el puntero de interfaz real. Cuando el objeto externo desea llamar a en el puntero de interfaz de un objeto interno, debe llamar a [**IGlobalInterfaceTable::GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), usar el puntero de interfaz devuelto y, a continuación, liberarlo. Cuando el objeto externo desaparece, debe llamar a [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) para quitar la interfaz de la tabla de interfaz global.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de la tabla de interfaz global](creating-the-global-interface-table.md)
</dt> </dl>

 

 