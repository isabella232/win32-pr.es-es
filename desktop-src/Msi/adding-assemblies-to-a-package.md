---
description: Windows Installer los desarrolladores pueden usar las instrucciones de este tema para crear Windows Installer paquetes que contienen ensamblados.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Agregar ensamblados a un paquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276533"
---
# <a name="adding-assemblies-to-a-package"></a>Agregar ensamblados a un paquete

Windows Installer los desarrolladores pueden usar las instrucciones de este tema para crear Windows Installer paquetes que contienen ensamblados.

Las siguientes directrices se aplican a los ensamblados Win32 y a los ensamblados que utiliza el Common Language Runtime de Microsoft .NET Framework.

-   Un componente Windows Installer no debe contener más de un ensamblado.
-   Todos los archivos del ensamblado deben estar en un único componente.
-   Cada componente que contiene un ensamblado debe tener una entrada en la tabla [MsiAssembly](msiassembly-table.md) .
-   El nombre seguro de la caché de ensamblados de cada ensamblado se debe crear en la tabla [MsiAssemblyName](msiassemblyname-table.md) .
-   Utilice la tabla [del registro](registry-table.md) en lugar de la tabla de [clase](class-table.md) al registrar la interoperabilidad com para un ensamblado.
-   Los ensamblados que tienen el mismo nombre seguro son el mismo ensamblado. Cuando diferentes aplicaciones instalan el mismo ensamblado, los componentes que contienen el ensamblado deben usar el mismo valor para el ComponentId en sus tablas de [componentes](component-table.md) .

> [!Note]  
> Los anuncios de productos identifican los ensamblados que pueden instalarse y usarse en distintas aplicaciones. Los anuncios de productos no identifican ensamblados privados.

 

## <a name="adding-win32-assemblies"></a>Agregar ensamblados Win32

Utilice las siguientes directrices al incluir ensamblados Win32:

-   El valor de ruta de rutas de la tabla de [componentes](component-table.md) para un componente que contiene un ensamblado Win32 no debe ser null.
-   El valor de ruta de acceso de la tabla de [componentes](component-table.md) para un componente que contiene un ensamblado de directiva Win32 debe ser el archivo de manifiesto.
-   El valor de ruta de acceso de la tabla de [componentes](component-table.md) para un componente que contiene un ensamblado de Win32, que no es un ensamblado de Directiva, no debe ser el archivo de manifiesto o el archivo de catálogo. Debe ser un archivo diferente en el ensamblado.
-   Agregue una fila a la tabla [MsiAssemblyName](msiassemblyname-table.md) para cada par de nombre y valor que se enumeran en la sección **assemblyIdentity** del manifiesto del ensamblado Win32.

## <a name="adding-assemblies-used-with-the-net-framework"></a>Agregar ensamblados utilizados con el .NET Framework

Utilice las siguientes directrices al incluir ensamblados que utiliza el Common Language Runtime de la .NET Framework.

-   El valor de ruta de rutas de la tabla de [componentes](component-table.md) para un componente que contiene el ensamblado no debe ser null.
-   Al instalar un ensamblado utilizado por el Common Language Runtime en la caché global de ensamblados, el valor de la \_ columna aplicación de archivo de la tabla MsiAssembly debe ser null.
-   Agregue una fila a la tabla [MsiAssemblyName](msiassemblyname-table.md) para cada atributo del nombre seguro del ensamblado. Todos los ensamblados deben tener el nombre, la versión y los atributos de referencia cultural que se especifican en la tabla MsiAssemblyName. Se requiere un atributo publicKeyToken para un ensamblado global. La tabla siguiente es un ejemplo de la tabla MsiAssemblyName para un ensamblado global que usa el Common Language Runtime.

[Tabla MsiAssemblyName](msiassemblyname-table.md)



| Componente  | Nombre           | Value            |
|------------|----------------|------------------|
| Componentea | Nombre           | simple           |
| Componentea | version        | 1.0.0.0          |
| Componentea | Referencia cultural        | neutral          |
| Componentea | publicKeyToken | 9d1ec8380f483f5a |



 

 

 



