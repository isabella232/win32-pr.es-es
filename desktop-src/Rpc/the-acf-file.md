---
title: El archivo ACF
description: El archivo ACF permite personalizar la interfaz RPC del cliente o de las aplicaciones de servidor sin que ello afecte a las características de red de la interfaz.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995584"
---
# <a name="the-acf-file"></a>El archivo ACF

El archivo ACF permite personalizar la interfaz RPC del cliente o de las aplicaciones de servidor sin que ello afecte a las características de red de la interfaz. Por ejemplo, si la aplicación cliente contiene una estructura de datos compleja que solo tiene significado en el equipo local, puede especificar en el archivo ACF cómo se pueden representar los datos de esa estructura en una forma independiente del equipo para las llamadas a procedimientos remotos.

En este tutorial se muestra otro uso del archivo ACF, que especifica el tipo de identificador de enlace que representa la conexión entre el cliente y el servidor. El **\[** atributo de [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) del **\]** encabezado ACF permite que la aplicación cliente seleccione un servidor para su llamada a procedimiento remoto. ACF define el identificador para que sea del identificador de [**tipo \_ t**](/windows/desktop/Midl/handle-t) (un tipo de datos primitivo de MIDL). El compilador MIDL colocará el nombre del identificador de enlace que especificó ACF, Hello \_ IfHandle en el archivo de encabezado que genera. Tenga en cuenta que este archivo ACF concreto tiene un cuerpo vacío.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

El compilador MIDL tiene una opción, [**/App \_ config**](/windows/desktop/Midl/-app-config), que le permite incluir determinados atributos ACF, como el **\_ identificador implícito**, en el archivo IDL, en lugar de crear un archivo ACF independiente. Considere la posibilidad de usar esta opción si la aplicación no requiere una gran cantidad de configuración especial y si la compatibilidad con OSF no es un problema.

 

 