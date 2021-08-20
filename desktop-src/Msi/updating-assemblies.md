---
description: La información de este tema identifica las directrices recomendadas para actualizar ensamblados mediante Windows del instalador.
ms.assetid: 60c70d48-aae2-4ea5-a880-ac9e2c83c28c
title: Actualizar ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65467613206f3736f35852a919432b11a6761860bd0db22c6da2600c159ef0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141628"
---
# <a name="updating-assemblies"></a>Actualizar ensamblados

La información de este tema identifica las directrices recomendadas para actualizar ensamblados mediante Windows del instalador.

Los autores de actualizaciones de ensamblados pueden usar las siguientes directrices, que se aplican a todos los tipos de ensamblados:

-   El método recomendado para actualizar un ensamblado es cambiar el nombre seguro del ensamblado en la [tabla MsiAssemblyName](msiassemblyname-table.md). La nueva versión del ensamblado la puede proporcionar un nuevo componente o el mismo componente que proporciona la versión anterior.
-   Si el mismo componente proporciona la nueva versión del ensamblado, no cambie el tipo de ensamblado de un ensamblado .NET Framework a un ensamblado Win32 o viceversa.
-   Si todas las aplicaciones del sistema deben usar el ensamblado actualizado, debe implementar un ensamblado de directiva. Un ensamblado de directiva puede redirigir las aplicaciones del sistema para que usen la nueva versión del ensamblado. Los ensamblados de directiva deben proporcionarse mediante la creación de un nuevo componente.
-   Windows Se requiere el instalador 3.0 o posterior para desinstalar las actualizaciones de ensamblados. Para obtener más información, [vea Quitar revisiones.](removing-patches.md)
-   La versión más reciente del ensamblado debe contener las mismas versiones o superiores de los archivos de ensamblados publicados anteriormente.
-   Windows Installer 3.0 puede .NET Framework ensamblados win32 mediante un reemplazo de archivo completo o por una actualización diferencial más pequeña. Para obtener más información, vea [Reducir el tamaño de revisión.](reducing-patch-size.md)
-   Si la actualización cambia el nombre seguro del ensamblado, se necesitan la tabla [MsiPatchOldAssemblyFile](msipatcholdassemblyfile-table.md) y la tabla [MsiPatchOldAssemblyName](msipatcholdassemblyname-table.md) si el paquete de revisión no tiene una tabla [MsiPatchSequence.](msipatchsequence-table.md) La tabla MsiPatchOldAssemblyFile y la tabla MsiPatchOldAssemblyName no son necesarias si el paquete de revisión tiene información de secuenciación de revisiones en una tabla MsiPatchSequence.
-   Antes de publicar una nueva revisión, pruebe la revisión apliquen con todas las revisiones publicadas anteriormente.

## <a name="updating-win32-assemblies"></a>Actualización de ensamblados win32

Use las siguientes directrices al actualizar ensamblados win32:

-   Cambie el nombre de seguridad del nuevo ensamblado que se especifica en la [tabla MsiAssemblyName](msiassemblyname-table.md).
-   Si desea que la aplicación use siempre la nueva versión del ensamblado sin que ello afecte a la versión de ensamblado usada por otras aplicaciones del sistema, use el mismo componente para contener la nueva versión de ensamblado que usó para la versión anterior del ensamblado. Mantenga el mismo ComponentId en la [tabla Component.](component-table.md) Después de aplicar revisiones a la aplicación, solo contiene una referencia a la nueva versión del ensamblado. La versión anterior del ensamblado puede permanecer con la nueva versión en la caché global de ensamblados. Esto no afecta a otras aplicaciones del sistema que usan la versión anterior del ensamblado. Cuando se usa el mismo componente para las versiones nuevas y antiguas del ensamblado, la actualización puede ser una revisión diferencial más pequeña.
-   Si la nueva versión del ensamblado no es compatible con todos los sistemas en los que desea instalar la aplicación, puede instalar las versiones nuevas y antiguas del ensamblado como ensamblados en paralelo. Para instalar ambas versiones de ensamblado en paralelo, cree un nuevo componente que contenga la nueva versión del ensamblado. El ComponentId de la [tabla Component](component-table.md) del nuevo componente debe ser diferente del ComponentId del componente con la versión anterior. Una vez que se aplica la revisión a la aplicación, contiene referencias a ambas versiones de ensamblado. A continuación, la aplicación se puede dirigir a la versión compatible del ensamblado mediante un manifiesto. Cuando se usan componentes diferentes para las versiones nuevas y antiguas del ensamblado, la actualización usa el reemplazo de archivos completo.

## <a name="updating-net-framework-assemblies"></a>Actualizar .NET Framework ensamblados

Use las siguientes directrices al actualizar .NET Framework ensamblados.

-   Cambie el nombre de seguridad del nuevo ensamblado que se especifica en la [tabla MsiAssemblyName](msiassemblyname-table.md).
-   Si desea que la aplicación use siempre la nueva versión del ensamblado sin que ello afecte a la versión del ensamblado usada por otras aplicaciones del sistema, cambie el nombre de seguridad del nuevo ensamblado especificado en la tabla [MsiAssemblyName](msiassemblyname-table.md)y use el mismo componente para contener la nueva versión del ensamblado que usó para la versión anterior del ensamblado. Mantenga el mismo ComponentId en la [tabla Component.](component-table.md) Después de aplicar revisiones a la aplicación, solo contiene una referencia a la nueva versión del ensamblado. La versión anterior del ensamblado puede permanecer con la nueva versión en la caché global. Esto no afecta a otras aplicaciones del sistema que usan la versión anterior del ensamblado. Cuando se usa el mismo componente para las versiones nuevas y antiguas del ensamblado, la actualización puede ser una revisión diferencial más pequeña.
-   Si la nueva versión del ensamblado no es compatible con todos los sistemas en los que desea instalar la aplicación, puede instalar las versiones nuevas y antiguas del ensamblado como ensamblados en paralelo. Para instalar ambas versiones de ensamblado en paralelo, cambie el nombre de seguridad del nuevo ensamblado que se especifica en la tabla [MsiAssemblyName](msiassemblyname-table.md)y cree un nuevo componente que contenga la nueva versión del ensamblado. El ComponentId de la [tabla Component](component-table.md) del nuevo componente debe ser diferente del ComponentId del componente con la versión anterior. Una vez que se aplica la revisión a la aplicación, contiene referencias a ambas versiones de ensamblado. A continuación, la aplicación se puede dirigir a la versión compatible del ensamblado mediante un manifiesto. Cuando se usan componentes diferentes para las versiones nuevas y antiguas del ensamblado, la actualización usa el reemplazo de archivos completo.
-   Una actualización local sobrescribe la copia de un ensamblado .NET Framework en la caché global de ensamblados. Este tipo de actualización de ensamblado no cambia el nombre de seguridad del ensamblado. Solo se cambia el valor del campo FileVersion de [la tabla MsiAssemblyName.](msiassemblyname-table.md) La actualización local de un ensamblado .NET Framework requiere .NET Framework 1.1 SP1 o superior.
    > [!Note]  
    > El tipo de actualización en contexto sobrescribe la copia del ensamblado en la caché global y puede interrumpir otras aplicaciones si la nueva versión del ensamblado no es totalmente compatible con versiones anteriores. El método recomendado para actualizar un ensamblado es cambiar el nombre seguro del ensamblado en la [tabla MsiAssemblyName](msiassemblyname-table.md).

     

 

 



