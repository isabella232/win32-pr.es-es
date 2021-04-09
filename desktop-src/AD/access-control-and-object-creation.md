---
title: Access Control y creación de objetos
description: El servidor de Active Directory no podrá crear un objeto secundario si el autor de la llamada no tiene el \_ derecho \_ ad \_ Create DS secundario \_ para ese tipo de objeto en el contenedor primario.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- Access Control y creación de objetos AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149153"
---
# <a name="access-control-and-object-creation"></a>Access Control y creación de objetos

El servidor de Active Directory no podrá crear un objeto secundario si el autor de la llamada no tiene **el \_ derecho \_ ad \_ Create \_ DS secundario** para ese tipo de objeto en el contenedor primario. Para determinar los tipos de objetos secundarios que el autor de la llamada puede crear en un objeto de directorio, lea el atributo **allowedChildClassesEffective** del objeto.

Cuando se usa el método [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) para crear un objeto secundario, el objeto no se hace persistente hasta que se llama a [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) en el nuevo objeto. Entre las llamadas a **Create** y **SetInfo** , el subproceso de creación puede colocar valores en cualquiera de las propiedades del nuevo objeto. Después de la llamada a **SetInfo** , el subproceso de creación no tiene necesariamente los derechos de acceso para establecer las propiedades del nuevo objeto. Para asegurarse de que el autor de la llamada tenga estos derechos, especifique un descriptor de seguridad explícito durante la creación. La DACL debe tener una ACE que proporcione al llamador los derechos de acceso necesarios en el objeto.

Para obtener más información sobre el control de acceso y la creación de objetos, vea [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](how-security-descriptors-are-set-on-new-directory-objects.md).

 

 