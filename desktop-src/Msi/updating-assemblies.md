---
description: La información de este tema identifica las directrices recomendadas para actualizar ensamblados con Windows Installer revisiones.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Actualizar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b185a9943ba20c81a1fa3431dd590eb05648c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083471"
---
# <a name="updating-assemblies"></a>Actualizar ensamblados

La información de este tema identifica las directrices recomendadas para actualizar ensamblados con Windows Installer revisiones.

Los autores de las actualizaciones de ensamblados pueden utilizar las siguientes directrices, que se aplican a todos los tipos de ensamblados:

-   El método recomendado para actualizar un ensamblado es cambiar el nombre seguro del ensamblado en la [tabla MsiAssemblyName](msiassemblyname-table.md). La nueva versión del ensamblado puede ser proporcionada por un componente nuevo o por el mismo componente que proporciona la versión anterior.
-   Si el mismo componente proporciona la nueva versión de ensamblado, no cambie el tipo de ensamblado de un ensamblado .NET Framework a un ensamblado Win32 o viceversa.
-   Si todas las aplicaciones del sistema deben usar el ensamblado actualizado, debe implementar un ensamblado de directiva. Un ensamblado de directivas puede redirigir las aplicaciones del sistema para usar la nueva versión de ensamblado. Los ensamblados de Directiva se deben proporcionar mediante la creación de un nuevo componente.
-   Se requiere Windows Installer 3,0 o posterior para desinstalar las actualizaciones de ensamblado. Para obtener más información, consulte [quitar revisiones](removing-patches.md).
-   La versión más reciente del ensamblado debe contener la misma versión o versiones posteriores de los archivos de los ensamblados publicados anteriormente.
-   Windows Installer 3,0 puede atender .NET Framework y ensamblados Win32 mediante un reemplazo de archivo completo o una actualización Delta más pequeña. Para obtener más información, consulte [reducir el tamaño](reducing-patch-size.md)de la revisión.
-   Si la actualización cambia el nombre seguro del ensamblado, se necesita la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) si el paquete de revisión no tiene una tabla [MsiPatchSequence](msipatchsequence-table.md) . La tabla MsiPatchOldAssemblyFile y la tabla MsiPatchOldAssemblyName no son necesarias si el paquete de revisión tiene información de secuenciación de revisiones en una tabla MsiPatchSequence.
-   Antes de lanzar una nueva revisión, probarla con todas las revisiones publicadas anteriormente.

## <a name="updating-win32-assemblies"></a>Actualizar ensamblados Win32

Utilice las siguientes directrices para actualizar ensamblados Win32:

-   Cambie el nombre seguro del nuevo ensamblado que se especifica en la [tabla MsiAssemblyName](msiassemblyname-table.md).
-   Si desea que la aplicación utilice siempre la nueva versión del ensamblado sin que afecte a la versión de ensamblado utilizada por otras aplicaciones del sistema, utilice el mismo componente para que contenga la nueva versión de ensamblado que usó para la versión anterior del ensamblado. Mantenga el mismo ComponentId en la tabla de [componentes](component-table.md) . Después de revisar la aplicación, solo contiene una referencia a la nueva versión del ensamblado. La versión anterior del ensamblado puede permanecer con la nueva versión en la caché global de ensamblados. Esto no afecta a otras aplicaciones del sistema que usan la versión anterior del ensamblado. Cuando se usa el mismo componente para las versiones nuevo y anterior del ensamblado, la actualización puede ser una revisión Delta más pequeña.
-   Si la nueva versión del ensamblado no es compatible con todos los sistemas en los que desea instalar la aplicación, puede instalar las versiones nuevas y antiguas del ensamblado como ensamblados en paralelo. Para instalar ambas versiones de ensamblado en paralelo, cree un componente nuevo que contenga la nueva versión de ensamblado. El ComponentId de la tabla de [componentes](component-table.md) para el nuevo componente debe ser diferente del ComponentID del componente con la versión anterior. Después de revisar la aplicación, contiene referencias a ambas versiones de ensamblado. A continuación, la aplicación se puede dirigir a la versión compatible del ensamblado mediante un manifiesto. Cuando se usan componentes diferentes para las versiones nuevas y anteriores del ensamblado, la actualización utiliza el reemplazo de archivos completo.

## <a name="updating-net-framework-assemblies"></a>Actualizar ensamblados de .NET Framework

Utilice las siguientes directrices para actualizar .NET Framework ensamblados.

-   Cambie el nombre seguro del nuevo ensamblado que se especifica en la [tabla MsiAssemblyName](msiassemblyname-table.md).
-   Si desea que la aplicación utilice siempre la nueva versión del ensamblado sin que afecte a la versión de ensamblado utilizada por otras aplicaciones del sistema, cambie el nombre seguro del nuevo ensamblado que se especifica en la [tabla MsiAssemblyName](msiassemblyname-table.md)y use el mismo componente para que contenga la nueva versión de ensamblado que usó para la versión anterior del ensamblado. Mantenga el mismo ComponentId en la tabla de [componentes](component-table.md) . Después de revisar la aplicación, solo contiene una referencia a la nueva versión del ensamblado. La versión anterior del ensamblado puede permanecer con la nueva versión en la caché global. Esto no afecta a otras aplicaciones del sistema que usan la versión anterior del ensamblado. Cuando se usa el mismo componente para las versiones nuevo y anterior del ensamblado, la actualización puede ser una revisión Delta más pequeña.
-   Si la nueva versión del ensamblado no es compatible con todos los sistemas en los que desea instalar la aplicación, puede instalar las versiones nuevas y antiguas del ensamblado como ensamblados en paralelo. Para instalar ambas versiones de ensamblado en paralelo, cambie el nombre seguro del nuevo ensamblado que se especifica en la [tabla MsiAssemblyName](msiassemblyname-table.md)y cree un componente nuevo que contenga la nueva versión de ensamblado. El ComponentId de la tabla de [componentes](component-table.md) para el nuevo componente debe ser diferente del ComponentID del componente con la versión anterior. Después de revisar la aplicación, contiene referencias a ambas versiones de ensamblado. A continuación, la aplicación se puede dirigir a la versión compatible del ensamblado mediante un manifiesto. Cuando se usan componentes diferentes para las versiones nuevas y anteriores del ensamblado, la actualización utiliza el reemplazo de archivos completo.
-   Una actualización en contexto sobrescribe la copia de un ensamblado de .NET Framework en la caché global de ensamblados. Este tipo de actualización de ensamblado no cambia el nombre seguro del ensamblado. Solo se cambia el valor del campo FileVersion de la [tabla MsiAssemblyName](msiassemblyname-table.md) . La actualización en contexto de un ensamblado de .NET Framework requiere .NET Framework 1,1 SP1 o posterior.
    > [!Note]  
    > El tipo en contexto de Update sobrescribe la copia del ensamblado en la memoria caché global y puede interrumpir otras aplicaciones si la nueva versión del ensamblado no es totalmente compatible con versiones anteriores. El método recomendado para actualizar un ensamblado es cambiar el nombre seguro del ensamblado en la [tabla MsiAssemblyName](msiassemblyname-table.md).

     

 

 



