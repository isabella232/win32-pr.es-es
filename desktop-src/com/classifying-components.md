---
title: Clasificar componentes
description: Clasificar componentes
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903710"
---
# <a name="classifying-components"></a>Clasificar componentes

Aunque un cliente puede examinar la lista de CLSID en el registro y seleccionar un componente que se va a usar, la carga de cada componente en el registro y la consulta de las interfaces compatibles son muy lentas. Para determinar si un componente admite las interfaces requeridas antes de crear una instancia del componente, se desarrolló un método para clasificar los componentes en categorías.

Una categoría de componente es un conjunto de interfaces a las que se ha asignado un GUID denominado CATId. Los componentes que implementan todas las interfaces de una categoría de componente se registran como miembros de esa categoría de componente. Los componentes que pertenecen a una determinada categoría de componentes se pueden seleccionar en el registro. Al registrarse como miembro de una categoría de componente, el componente garantiza que admita todas las interfaces de miembro de la categoría de componentes.

Un componente puede ser un miembro de muchas categorías. No se limita a admitir interfaces en una categoría de componentes. Puede admitir cualquier interfaz, además de las de una categoría de componente.

A diferencia del registro estándar de componentes, en el que los desarrolladores deben escribir código que registre los objetos manualmente, la categoría de componentes automatiza gran parte de este trabajo. Los seis métodos de la interfaz [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definen categorías de componentes y registran objetos que los implementan o requieren. El objeto de [Administrador de categorías de componentes](the-component-categories-manager.md) implementa esta interfaz. Vea **ICatRegister** y [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) para obtener información adicional sobre el uso de categorías de componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 




