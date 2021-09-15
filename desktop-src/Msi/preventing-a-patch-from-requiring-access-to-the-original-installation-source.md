---
description: No es posible eliminar todas las circunstancias en las que la aplicación de una revisión puede requerir acceso al origen de instalación original.
ms.assetid: f7028c55-e4a5-4596-af7a-728c9f4f367e
title: Impedir que una revisión requiera acceso al origen de instalación original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baee8b261ff0a3f6bb94fb141ee765726ffa2ced
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473958"
---
# <a name="preventing-a-patch-from-requiring-access-to-the-original-installation-source"></a>Impedir que una revisión requiera acceso al origen de instalación original

No es posible eliminar todas las circunstancias en las que la aplicación de una revisión puede requerir acceso al origen de instalación original.

Siga los siguientes puntos para minimizar la posibilidad de que la revisión requiera acceso al origen original:

-   Use solo revisiones de archivos completos. Esto elimina la necesidad de crear revisiones binarias para todas las versiones publicadas anteriormente del archivo. Tenga en cuenta que las revisiones de archivos completos suelen tener un tamaño mayor que las revisiones binarias. Puede establecer fácilmente una revisión para que sea una revisión de archivo completa mediante la creación de la propiedad IncludeWholeFilesOnly con un valor de 1 (uno) en el archivo De propiedades de creación de revisiones (PATCH).
-   Asegúrese de que ninguna de las acciones personalizadas acceda a la ubicación de origen original.
-   Asegúrese de que la acción ResolveSource está condicionalizada para que solo se ejecute cuando sea necesario o, como alternativa, no esté presente en absoluto.
-   Rellene la [tabla MsiFileHash para](msifilehash-table.md) todos los archivos sin versión. La Windows SDK del instalador de Msifiler.exe, puede hacerlo fácilmente.
-   Asegúrese de que todos los archivos tienen la versión y la información de idioma correctas. La Windows SDK del instalador de Msifiler.exe, puede hacerlo fácilmente.

## <a name="source-requirements-when-patching"></a>Requisitos de origen al aplicar revisiones

Es posible que se requiera acceso a los orígenes de instalación originales para aplicar la revisión en los casos siguientes:

-   La revisión se aplica a una característica que se ejecuta actualmente desde el origen. En este caso, la característica se pasa del estado run-from-source al estado local.
-   La revisión se aplica a un componente que tiene un archivo que falta o está dañado.
-   La revisión se aplica a un archivo de un componente que también contiene archivos sin versión sin entradas MsiFileHash. Se requiere una [tabla MsiFileHash](msifilehash-table.md) rellena para evitar que se vuelvan a copiar archivos sin versión innecesarias desde la ubicación de origen.
-   La revisión se aplicó con un REINSTALLMODE de amus o emus. Esta opción es peligrosa porque realiza operaciones de copia de archivos independientemente de la versión del archivo. Esto puede dar lugar a la revocación de archivos y casi siempre requiere el origen. El valor DE REINSTALLMODE recomendado es omus.
-   Falta el paquete almacenado en caché para el producto. El paquete almacenado en caché es necesario para la aplicación de una revisión. El paquete almacenado en caché se almacena en la carpeta %windir% \\ Installer.
-   El paquete se ha escrito para realizar una llamada a la [acción ResolveSource](resolvesource-action.md). Por lo general, esta acción debe evitarse o condicionalizarse adecuadamente, ya que su ejecución siempre da como resultado un acceso al origen.
-   El paquete tiene una acción personalizada que intenta acceder al origen de alguna manera. El ejemplo más común es una acción personalizada de instalación simultánea de tipo 23.
    > [!Note]  
    > No se recomiendan las instalaciones simultáneas para la instalación de aplicaciones destinadas a la versión pública. Para obtener información sobre las instalaciones simultáneas, vea [Instalaciones simultáneas.](concurrent-installations.md)

     

-   El paquete de revisión consta de revisiones binarias que no se aplican a la versión actual del archivo en el equipo.

Tenga en cuenta el ejemplo siguiente Windows instalador requiere acceso al origen original al aplicar una revisión:

1.  Instale la versión RTM del ejemplo del producto.
2.  Aplique la revisión Qfe1.msp al equipo. Esto hace revisiones a la versión 1.0 de Example.dll a la versión 1.1.
3.  Se proporciona una nueva revisión, Qfe2.msp, que actualiza Example.dll a la versión 1.2 y queda obsoleta Qfe1.msp. Sin embargo, la revisión solo se creó para la versión de destino 1.0 de Example.dll porque se generó mediante la versión RTM del producto. Example.dll versión 1.2 incluye la corrección contenida en la versión 1.1 de Example.dll, pero el archivo .msp se generó entre las imágenes RTM y QFE2. Por lo tanto, cuando Qfe2.msp se aplica al equipo, Windows instalador debe tener acceso al origen original. La revisión binaria para Example.dll no se puede aplicar a la versión 1.1; solo se puede aplicar a la versión 1.0. Como resultado, el instalador vuelve a copiar la versión 1.0 de Example.dll desde la ubicación de origen original para que la revisión se pueda aplicar correctamente.

## <a name="source-requirements-when-removing-a-patch"></a>Requisitos de origen al quitar una revisión

Es posible que se requiera acceso a los orígenes de instalación originales para quitar una revisión si el instalador de Windows no ha almacenado información de línea de base sobre la revisión. A partir Windows Installer 3.0, el instalador guarda selectivamente la información de línea de base sobre los archivos cuando se actualizan. Para obtener más información sobre la memoria caché de línea de base, vea [Reducción del tamaño de revisión.](reducing-patch-size.md)

 

 



