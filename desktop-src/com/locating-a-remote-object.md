---
title: Buscar un objeto remoto
description: Buscar un objeto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127249260"
---
# <a name="locating-a-remote-object"></a>Buscar un objeto remoto

Con la llegada de COM para sistemas [distribuidos,](com-class-objects-and-clsids.md) COM usa el modelo básico para la creación de objetos descritos en Objetos de clase COM y CLID y agrega más de una manera de localizar un objeto que podría residir en otro sistema de una red, sin sobrecargar la aplicación cliente.

COM ha agregado claves del Registro que permiten a un servidor registrar el nombre de la máquina en la que reside o la máquina donde se encuentra un almacenamiento existente. Por lo tanto, las aplicaciones cliente solo necesitan conocer el CLSID del servidor.

Sin embargo, para los casos en los que se desea, COM ha reemplazado un parámetro reservado previamente de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) por una estructura [**COSERVERINFO,**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) que permite a un cliente especificar la ubicación de un servidor. Otro valor importante de la función **CoGetClassObject** es la enumeración [**CLSCTX,**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) que especifica si el objeto esperado se va a ejecutar en proceso, fuera de proceso local o fuera de proceso remoto. Juntos, estos dos valores y los valores del Registro determinan cómo y dónde se va a ejecutar el objeto.

> [!Note]  
> Las llamadas de creación de instancias, cuando especifican una ubicación de servidor, pueden invalidar una configuración del Registro. El algoritmo COM que usa para hacerlo se describe en la referencia de la [**enumeración CLSCTX.**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)

 

La activación remota depende de la relación de seguridad entre el cliente y el servidor. Para obtener más información, vea [Seguridad en COM.](security-in-com.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de clase COM y CLSID](com-class-objects-and-clsids.md)
</dt> <dt>

[Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 