---
title: El archivo ACF
description: El archivo ACF permite personalizar la interfaz RPC de las aplicaciones cliente o servidor sin que ello afecte a las características de red de la interfaz.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d234b30c25870dd7a21cb790cc4839236ab69093291285b64c870cf7c05cb11f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080845"
---
# <a name="the-acf-file"></a>El archivo ACF

El archivo ACF permite personalizar la interfaz RPC de las aplicaciones cliente o servidor sin que ello afecte a las características de red de la interfaz. Por ejemplo, si la aplicación cliente contiene una estructura de datos compleja que solo tiene significado en el equipo local, puede especificar en el archivo ACF cómo se pueden representar los datos de esa estructura en un formato independiente de la máquina para las llamadas a procedimiento remoto.

En este tutorial se muestra otro uso del archivo ACF, especificando el tipo de identificador de enlace que representa la conexión entre el cliente y el servidor. El **\[** [**atributo de \_ identificador**](/windows/desktop/Midl/implicit-handle) **\]** implícito en el encabezado ACF permite a la aplicación cliente seleccionar un servidor para su llamada a procedimiento remoto. El ACF define el identificador que debe ser del tipo [**handle \_ t**](/windows/desktop/Midl/handle-t) (un tipo de datos primitivo MIDL). El compilador MIDL colocará el nombre del identificador de enlace especificado por el ACF, hello IfHandle en el archivo \_ de encabezado que genera. Observe que este archivo ACF concreto tiene un cuerpo vacío.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

El compilador MIDL tiene una opción, [**/app \_ config**](/windows/desktop/Midl/-app-config), que permite incluir determinados atributos de ACF, como el identificador implícito, en el archivo IDL, en lugar de crear un archivo ACF independiente. **\_** Considere la posibilidad de usar esta opción si la aplicación no requiere una gran cantidad de configuración especial y si la compatibilidad estricta de OSF no es un problema.

 

 