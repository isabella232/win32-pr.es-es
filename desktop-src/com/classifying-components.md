---
title: Clasificación de componentes
description: Clasificación de componentes
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e8382c1cbada72c2a8ab480ded78702424736850299b9e5e9fad7b328e3280
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048713"
---
# <a name="classifying-components"></a>Clasificación de componentes

Aunque un cliente puede examinar la lista de CLID del Registro y seleccionar un componente que se va a usar, cargar cada componente del registro y consultarlo para sus interfaces admitidas lleva mucho tiempo. Para determinar si un componente admite las interfaces necesarias antes de crear una instancia del componente, se desarrolló un método para clasificar los componentes en categorías.

Una categoría de componente es un conjunto de interfaces a las que se ha asignado un GUID denominado CATID. Los componentes que implementan todas las interfaces de una categoría de componente se registran como miembros de esa categoría de componentes. Los componentes que pertenecen a una determinada categoría de componentes se pueden seleccionar en el Registro. Al registrarse como miembro de una categoría de componente, el componente garantiza que admite todas las interfaces miembro de la categoría de componentes.

Un componente puede ser miembro de muchas categorías. No se limita a admitir interfaces en una categoría de componentes. Puede admitir cualquier interfaz, además de las de una categoría de componentes.

A diferencia del registro estándar de componentes, en el que los desarrolladores deben escribir código que registre manualmente objetos, las categorías de componentes automatizan gran parte de este trabajo. Los seis métodos de la [**interfaz ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) definen categorías de componentes y registran objetos que las implementan o las requieren. El [objeto Administrador de categorías de](the-component-categories-manager.md) componentes implementa esta interfaz. Consulte **ICatRegister** e [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) para obtener información adicional sobre el uso de categorías de componentes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 




