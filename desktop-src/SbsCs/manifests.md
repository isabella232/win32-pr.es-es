---
description: Los manifiestos son archivos XML que acompañan y describen ensamblados en paralelo o aplicaciones aisladas.
ms.assetid: 53c4c2e6-fff9-4506-b7e0-d091d2ec9883
title: Manifiestos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974aaea3dad60c80456d0acd085d610c81b93716342962abcd465adaf9efdf48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977215"
---
# <a name="manifests"></a>Manifiestos

Los manifiestos son archivos XML que acompañan y describen ensamblados en paralelo o aplicaciones aisladas. Los manifiestos identifican de forma única el ensamblado a través del **elemento assemblyIdentity del** ensamblado. Contienen información que se usa para el enlace y la activación, como clases COM, interfaces y bibliotecas de tipos, que tradicionalmente se ha almacenado en el Registro. Los manifiestos también especifican los archivos que constituyen el ensamblado y pueden incluir Windows clases si el autor del ensamblado quiere que se les controle la versión. Los ensamblados en paralelo no están registrados en el sistema, pero están disponibles para las aplicaciones y otros ensamblados del sistema que especifican dependencias en los archivos de manifiesto.

Los archivos de manifiesto permiten a los administradores y las aplicaciones administrar versiones de ensamblado en paralelo después de la implementación. Cada ensamblado en paralelo debe tener un manifiesto asociado. La instalación de Windows XP instala los ensamblados en paralelo de [Microsoft](supported-microsoft-side-by-side-assemblies.md) compatibles con sus manifiestos. Si desarrolla sus propios ensamblados en paralelo, también debe instalar archivos de manifiesto. Para obtener más información, vea [Instalación de ensamblados](installing-side-by-side-assemblies.md) en paralelo y referencia de [archivos de manifiesto.](manifest-files-reference.md)

Los manifiestos y los archivos de configuración no están localizados.

Los siguientes tipos de manifiestos se usan con ensamblados en paralelo:

-   [Los manifiestos de](assembly-manifests.md) ensamblado describen los ensamblados en paralelo. Se usan para administrar los nombres, las versiones, los recursos y los ensamblados dependientes de los ensamblados en paralelo. Los manifiestos de [ensamblados compartidos](/windows/desktop/Msi/shared-assemblies) se almacenan en la carpeta WinSxS del sistema. Los manifiestos de ensamblado privado se almacenan como un recurso en el archivo DLL o en la carpeta de la aplicación.
-   [Los manifiestos de aplicación](application-manifests.md) describen [las aplicaciones aisladas.](isolated-applications.md) Se usan para administrar los nombres y versiones de los ensamblados en paralelo compartidos a los que se debe enlazar la aplicación en tiempo de ejecución. Los manifiestos de aplicación se copian en la misma carpeta que el archivo ejecutable de la aplicación o se incluyen como un recurso en el archivo ejecutable de la aplicación.
-   [Los archivos de configuración de](application-configuration-files.md)la aplicación son manifiestos que se usan para invalidar y redirigir las versiones de ensamblados dependientes que usan las aplicaciones y ensamblados en paralelo.
-   [Publisher archivos de configuración](publisher-configuration-files.md)de , son manifiestos que se usan para redirigir la versión de un ensamblado en paralelo a otra versión compatible. La versión a la que se redirige el ensamblado debe tener los mismos valores major.minor que la versión original.

 

 
