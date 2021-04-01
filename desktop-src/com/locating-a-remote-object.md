---
title: Buscar un objeto remoto
description: Buscar un objeto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103904861"
---
# <a name="locating-a-remote-object"></a>Buscar un objeto remoto

Con la llegada de COM para sistemas distribuidos, COM usa el modelo básico para la creación de objetos descrito en [objetos de clase com y CLSID](com-class-objects-and-clsids.md) y agrega más de una manera de buscar un objeto que puede residir en otro sistema de una red, sin sobrecargar la aplicación cliente.

COM ha agregado claves del registro que permiten que un servidor registre el nombre del equipo en el que reside o el equipo en el que se encuentra un almacenamiento existente. Por lo tanto, las aplicaciones cliente solo necesitan conocer el CLSID del servidor.

Sin embargo, para los casos en los que se desea, COM ha reemplazado a un parámetro reservado previamente de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) con una estructura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , que permite a un cliente especificar la ubicación de un servidor. Otro valor importante de la función **CoGetClassObject** es la enumeración [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , que especifica si el objeto esperado se va a ejecutar en proceso, local fuera de proceso o remoto fuera de proceso. En conjunto, estos dos valores y los valores del registro determinan cómo y dónde se va a ejecutar el objeto.

> [!Note]  
> Las llamadas de creación de instancia, cuando especifican una ubicación de servidor, pueden invalidar una configuración del registro. El algoritmo que utiliza COM para ello se describe en la referencia de la enumeración [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .

 

La activación remota depende de la relación de seguridad entre el cliente y el servidor. Para obtener más información, vea [seguridad en com](security-in-com.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de clase COM y CLSID](com-class-objects-and-clsids.md)
</dt> <dt>

[Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 