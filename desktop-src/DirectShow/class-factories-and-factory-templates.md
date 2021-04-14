---
description: En este tema se describe cómo implementar un archivo DLL para un filtro DirectShow mediante las clases base de DirectShow.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Generadores de clases y plantillas de generador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02699a8ff0740ddcf1d86b8514fd45dac9e32ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555613"
---
# <a name="class-factories-and-factory-templates"></a>Generadores de clases y plantillas de generador

En este tema se describe cómo implementar un archivo DLL para un filtro DirectShow mediante las [clases base de DirectShow](directshow-base-classes.md).

Antes de que un cliente cree una instancia de un objeto COM, crea una instancia del generador de clases del objeto mediante una llamada a la función [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Después, el cliente llama al método **IClassFactory:: CreateInstance** del generador de clases. Es el generador de clases que crea realmente el componente y devuelve un puntero a la interfaz solicitada. (La función [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) combina estos pasos, dentro de la llamada de función).

En la ilustración siguiente se muestra la secuencia de llamadas a métodos.

![llamadas al método para crear un generador de clases](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) llama a la función [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , que se define en el archivo dll. Esta función crea el generador de clases y devuelve un puntero a una interfaz en el generador de clases. DirectShow implementa **DllGetClassObject** , pero la función se basa en el código de una manera determinada. Para entender cómo funciona, debe entender cómo implementa DirectShow los generadores de clases.

Un generador de clases es un objeto COM dedicado a la creación de otro objeto COM. Cada generador de clases tiene un tipo de objeto que crea. En DirectShow, cada generador de clases es una instancia de la misma clase de C++, **CClassFactory**. Los generadores de clases se especializan por medio de otra clase, [**CFactoryTemplate**](cfactorytemplate.md), también denominada *plantilla de fábrica*. Cada generador de clases contiene un puntero a una plantilla de fábrica. La plantilla de generador contiene información sobre un componente específico, como el identificador de clase (CLSID) del componente, y un puntero a una función que crea el componente.

El archivo DLL declara una matriz global de plantillas de fábrica, una para cada componente del archivo DLL. Cuando [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crea un nuevo generador de clases, busca una plantilla con un CLSID coincidente en la matriz. Suponiendo que encuentra una, crea un generador de clases que contiene un puntero a la plantilla coincidente. Cuando el cliente llama a **IClassFactory:: CreateInstance**, el generador de clases llama a la función de creación de instancias definida en la plantilla.

En la ilustración siguiente se muestra la secuencia de llamadas a métodos.

![plantillas de generador de clases en un archivo dll](images/classfactory2.png)

La ventaja de esta arquitectura es que puede definir solo algunas cosas que son específicas del componente, como la función de creación de instancias, sin implementar el generador de clases completo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo crear un archivo DLL de filtro de DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
