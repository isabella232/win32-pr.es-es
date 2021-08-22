---
description: Windows Los desarrolladores del instalador pueden usar las instrucciones de este tema para crear Windows paquetes del instalador que contienen ensamblados.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Agregar ensamblados a un paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a96c1b8c8d9b73fedf03fceeb82be62b8457556da02334ed7a224aefc2202a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534875"
---
# <a name="adding-assemblies-to-a-package"></a>Agregar ensamblados a un paquete

Windows Los desarrolladores del instalador pueden usar las instrucciones de este tema para crear Windows paquetes del instalador que contienen ensamblados.

Las siguientes directrices se aplican a los ensamblados Win32 y a los ensamblados que common language runtime de microsoft .NET Framework usa.

-   Un Windows installer no debe contener más de un ensamblado.
-   Todos los archivos del ensamblado deben estar en un solo componente.
-   Cada componente que contiene un ensamblado debe tener una entrada en la [tabla MsiAssembly.](msiassembly-table.md)
-   El nombre de caché de ensamblados segura de cada ensamblado debe crearse en la [tabla MsiAssemblyName.](msiassemblyname-table.md)
-   Use la [tabla Registry](registry-table.md) en lugar de la [tabla Class](class-table.md) al registrar la interoperabilidad COM para un ensamblado.
-   Los ensamblados que tienen el mismo nombre de seguridad son el mismo ensamblado. Cuando diferentes aplicaciones instalan el mismo ensamblado, los componentes que contienen el ensamblado deben usar el mismo valor para ComponentId en sus [tablas component.](component-table.md)

> [!Note]  
> Los anuncios de productos identifican los ensamblados que se pueden instalar y usar en distintas aplicaciones. Los anuncios de productos no identifican ensamblados privados.

 

## <a name="adding-win32-assemblies"></a>Agregar ensamblados Win32

Use las siguientes directrices al incluir ensamblados Win32:

-   El valor de KeyPath de la [tabla Component](component-table.md) de un componente que contiene un ensamblado Win32 no debe ser Null.
-   El valor keyPath de la [tabla Component](component-table.md) de un componente que contiene un ensamblado de directiva Win32 debe ser el archivo de manifiesto.
-   El valor keyPath de la tabla [Component](component-table.md) de un componente que contiene un ensamblado Win32, que no es un ensamblado de directiva, no debe ser el archivo de manifiesto o el archivo de catálogo. Debe ser un archivo diferente en el ensamblado.
-   Agregue una fila a la [tabla MsiAssemblyName](msiassemblyname-table.md) para cada par de nombre y valor que se enumeran en la sección **assemblyIdentity** del manifiesto del ensamblado Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Agregar ensamblados usados con el .NET Framework

Use las instrucciones siguientes al incluir ensamblados que common language runtime del .NET Framework utiliza.

-   El valor de KeyPath de la [tabla Component](component-table.md) de un componente que contiene el ensamblado no debe ser Null.
-   Al instalar un ensamblado usado por Common Language Runtime en la caché global de ensamblados, el valor de la columna Aplicación de archivo de la tabla \_ MsiAssembly debe ser Null.
-   Agregue una fila a la [tabla MsiAssemblyName](msiassemblyname-table.md) para cada atributo del nombre de seguridad del ensamblado. Todos los ensamblados deben tener los atributos Name, Version y Culture que se especifican en la tabla MsiAssemblyName. Se requiere un atributo publicKeyToken para un ensamblado global. La tabla siguiente es un ejemplo de la tabla MsiAssemblyName para un ensamblado global que Common Language Runtime usa.

[Tabla MsiAssemblyName](msiassemblyname-table.md)



| Componente  | Nombre           | Valor            |
|------------|----------------|------------------|
| Componente A | Nombre           | simple           |
| Componente A | version        | 1.0.0.0          |
| Componente A | culture        | neutral          |
| Componente A | Publickeytoken | 9d1ec8380f483f5a |



 

 

 



