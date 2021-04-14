---
title: Clases, objetos e interfaces
description: Clases, objetos e interfaces
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104488506"
---
# <a name="classes-objects-and-interfaces"></a>Clases, objetos e interfaces

En el lenguaje de programación C++, una *clase* consta de *propiedades* (o datos de miembro) y *métodos* (o funciones miembro). Las propiedades son elementos de datos, como los contenidos en una estructura. Los métodos se utilizan para una variedad de propósitos, como la inicialización, la asignación, las operaciones y el acceso a datos. Se utiliza una declaración de clase de la misma manera que se utiliza una declaración de estructura. La memoria se asigna a una clase cuando se define un *objeto* de clase. Cada objeto de clase tiene un área de datos para sus propiedades y una tabla de punteros a los métodos que admite.

En OLE, un objeto consta de datos y métodos, como en C++. Sin embargo, un objeto OLE cumple las reglas más estrictas. Los datos son estrictamente internos. Un objeto solo expone interfaces. Una *interfaz* es un conjunto de métodos relacionados para un objeto. Cada objeto puede admitir varias interfaces. Todas las interfaces OLE admiten la interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

 

 




