---
description: ICE62 realiza exhaustivas comprobaciones en la tabla IsolatedComponent para los datos que pueden provocar un comportamiento inesperado.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb5c2fd3f3305c791851fb3bd7480edc5e17f361c40719e8091930188dfa991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528245"
---
# <a name="ice62"></a>ICE62

ICE62 realiza exhaustivas comprobaciones en la [tabla IsolatedComponent para](isolatedcomponent-table.md) los datos que pueden provocar un comportamiento inesperado.

Si no se corrige un error notificado por ICE62, se puede producir un error en el sistema de componentes aislados de una amplia variedad de maneras. Por ejemplo, si el bit SharedDllRefCount no está establecido para un componente compartido, el registro del componente podría quitarse cuando otra aplicación use ese ComponentId y se desinstale.

## <a name="result"></a>Resultado

ICE62 envía una advertencia o un error cuando encuentra datos en la tabla IsolatedComponent que pueden producir un comportamiento inesperado.

## <a name="example"></a>Ejemplo

ICE62 notifica los siguientes errores y advertencias para los ejemplos mostrados.

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

Component2 aparece como componente de aplicación para el aislamiento de component1. Sin embargo, Component2 tiene una ruta de acceso de clave del Registro y no proporciona una ruta de acceso ejecutable válida para usar para aislar el componente.

Para corregir este error, use un componente diferente como aplicación para el componente aislado Component1.

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

Component1 aparece como un componente compartido aislado, pero no tiene el conjunto de bits SharedDllRefCount. Esto podría dar lugar a que la duración del componente sea incorrecta. Si otra aplicación usa este componente (aislado o no) y se desinstala, se quita el registro del componente, pero permanece la copia aislada de esta aplicación. Esto provoca problemas de reparación y desinstalación.

Para corregir este error, establezca el bit SharedDllRefCount del componente.

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

Component1 y Component2 se instalan mediante diferentes características. Component1 se instala mediante Feature1 y Component2 lo instala Feature2. Feature1 no es un elemento primario de Feature2, por lo que es posible que la aplicación se instale, pero no el componente aislado, lo que romperá el aislamiento.

Para corregir este error, agregue una entrada a la tabla FeatureComponents que vincule Component1 a la misma característica que (o una característica primaria de) la característica que instala Component2.

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

Component1 tiene una condición en la tabla Component. Si esta condición cambia alguna vez de TRUE a FALSE durante la duración de una instalación en un equipo, el componente aislado podría quedar huérfano sin información de registro.

Para corregir esta advertencia, quite la condición o cree la condición para que nunca pueda cambiar de TRUE a FALSE.

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

Component1 está aislado para Component2 y Component3, y los dos componentes también se instalan en el mismo directorio. Las aplicaciones comparten un componente aislado, pero si se quita una aplicación, el componente compartido también hace que las demás aplicaciones pierdan el componente aislado.

Para corregir esta advertencia, instale las aplicaciones en directorios diferentes o compruebe si algunas de las aplicaciones realmente requieren un componente aislado.

[Tabla IsolatedComponent](isolatedcomponent-table.md)



| Componente \_ compartido | Aplicación \_ de componentes |
|-------------------|------------------------|
| Componente1        | Componente 2             |
| Componente1        | Componente 3             |



 

[Tabla de componentes](component-table.md)



| Componente  | Componentid | Directorio\_ | Atributos | Condición   | KeyPath   |
|------------|-------------|-------------|------------|-------------|-----------|
| Componente1 |             | Dir1        | 0          | MYCONDITION | Archivo1     |
| Componente 2 |             | TARGETDIR   | 4          |             | Registry2 |
| Componente 3 |             | TARGETDIR   | 0          |             | File3     |



 

[FeatureComponentsTable](featurecomponents-table.md)



| Característica\_ | Componente\_ |
|-----------|-------------|
| Característica 1  | Componente1  |
| Característica 2  | Componente 2  |
| Característica 1  | Componente 3  |



 

[Tabla de características](feature-table.md) (parcial)



| Característica  | Elemento \_ primario de la característica |
|----------|-----------------|
| Característica 1 |                 |
| Característica 2 |                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



