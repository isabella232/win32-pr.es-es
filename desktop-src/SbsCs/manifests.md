---
description: Los manifiestos son archivos XML que acompañan y describen ensamblados en paralelo o aplicaciones aisladas.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifiestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2536e518f39791b400b9e99002b9575f4428d64d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652565"
---
# <a name="manifests"></a>Manifiestos

Los manifiestos son archivos XML que acompañan y describen ensamblados en paralelo o aplicaciones aisladas. Los manifiestos identifican de forma única el ensamblado a través del elemento **assemblyIdentity** del ensamblado. Contienen información utilizada para el enlace y la activación, como clases, interfaces y bibliotecas de tipos COM, que tradicionalmente se han almacenado en el registro. Los manifiestos también especifican los archivos que componen el ensamblado y pueden incluir clases de Windows si el autor del ensamblado desea tener versiones. Los ensamblados en paralelo no están registrados en el sistema, pero están disponibles para las aplicaciones y otros ensamblados del sistema que especifican las dependencias en los archivos de manifiesto.

Los archivos de manifiesto permiten a los administradores y las aplicaciones administrar versiones de ensamblados en paralelo después de la implementación. Cada ensamblado simultáneo debe tener un manifiesto asociado. La instalación de Windows XP instala los [ensamblados en paralelo de Microsoft compatibles](supported-microsoft-side-by-side-assemblies.md) con sus manifiestos. Si desarrolla sus propios ensamblados en paralelo, también debe instalar los archivos de manifiesto. Para obtener más información, consulte la referencia sobre la [instalación de ensamblados en paralelo](installing-side-by-side-assemblies.md) y [archivos de manifiesto](manifest-files-reference.md).

Los manifiestos y los archivos de configuración no están localizados.

Los siguientes tipos de manifiestos se utilizan con ensamblados en paralelo:

-   Los [manifiestos de ensamblado](assembly-manifests.md) describen los ensamblados en paralelo. Se usan para administrar los nombres, las versiones, los recursos y los ensamblados dependientes de los ensamblados en paralelo. Los manifiestos de [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) se almacenan en la carpeta WinSxS del sistema. Los manifiestos de ensamblado privados se almacenan como un recurso en el archivo DLL o en la carpeta de la aplicación.
-   Los [manifiestos de aplicación](application-manifests.md) describen [las aplicaciones aisladas](isolated-applications.md). Se usan para administrar los nombres y las versiones de los ensamblados en paralelo compartidos a los que se debe enlazar la aplicación en tiempo de ejecución. Los manifiestos de aplicación se copian en la misma carpeta que el archivo ejecutable de la aplicación o se incluyen como un recurso en el archivo ejecutable de la aplicación.
-   [Los archivos de configuración](application-configuration-files.md)de la aplicación, son manifiestos que se usan para invalidar y redirigir las versiones de los ensamblados dependientes que usan los ensamblados en paralelo y las aplicaciones.
-   [Los archivos de configuración del publicador](publisher-configuration-files.md)son manifiestos que se usan para redirigir la versión de un ensamblado simultáneo a otra versión compatible. La versión a la que se redirige el ensamblado debe tener los mismos valores. minor principales que la versión original.

 

 
