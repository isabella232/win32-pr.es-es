---
title: Ver contenedores como nodos de hoja
description: Cualquier objeto de Active Directory Domain Services puede ser un contenedor de otros objetos.
ms.assetid: 38300ca5-745a-4640-9723-6052a9843f45
ms.tgt_platform: multiple
keywords:
- Ver contenedores como nodos de hoja
- contenedores AD, ver como nodos de hoja
- AD hoja, ver contenedores como nodos hoja
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1631526ed78132829a7576960a997b13cc232b5f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104358795"
---
# <a name="viewing-containers-as-leaf-nodes"></a>Ver contenedores como nodos de hoja

Cualquier objeto de Active Directory Domain Services puede ser un contenedor de otros objetos. Esto puede abarrotar la interfaz de usuario, por lo que es posible declarar que un objeto de una clase específica solo se muestre como una hoja en la interfaz de usuario. El atributo **treatAsLeaf** es un atributo de especificador de presentación de un solo valor que determina si los objetos de esa clase deben mostrarse solo como objetos hoja. Este atributo es un valor booleano que, si **es true**, indica que los objetos de la clase deben mostrarse solo como elementos hoja. Si **es false**, indica que los objetos de la clase se pueden mostrar como un contenedor o una hoja. Al igual que todos los atributos de especificadores de presentación, el atributo **treatAsLeaf** se establece en función de la configuración regional, por lo que este atributo se puede localizar según sea necesario. Por ejemplo, la **visualización de usuario** para el especificador de pantalla Configuración regional en inglés (0409) tiene el atributo **TreatAsLeaf** establecido en **true** de forma predeterminada. Esto hace que la interfaz de usuario muestre todos los objetos de **usuario** como objetos hoja.

**Para establecer el valor del atributo **treatAsLeaf****

1.  Enlazar al atributo de visualización deseado en la configuración regional deseada. Para obtener más información y un ejemplo de código, vea [contenedor DisplaySpecifiers](displayspecifiers-container.md).
2.  Use el método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) para establecer el atributo **treatAsLeaf** en **true** o **false**.
3.  Para confirmar los cambios en el directorio, llame al método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) .

 

 