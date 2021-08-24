---
title: Desarrollo de una aplicación OEM que usa un archivo personalizado
description: Obtenga información sobre cómo desarrollar una aplicación que usa un archivo personalizado para pasar información del OEM a la aplicación.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4780e930d057c325038c94dc86fc375c70bdb1cc8dca34ac6169436bc0f0e323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855325"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Desarrollo de una aplicación OEM que usa un archivo personalizado

Para obtener más información sobre cómo crear y usar archivos de datos personalizados, vea [DISM App Package (.appx o .appxbundle) Servicing Command-Line Options](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Obtenga información sobre cómo desarrollar una aplicación que usa un archivo personalizado para pasar información del OEM a la aplicación.

En el caso de las aplicaciones que cree para la implementación de OEM, puede usar un archivo personalizado para pasar información del OEM a las aplicaciones. Para pasar información de OEM a una aplicación, cree un archivo Custom.data en microsoft.syscarpeta tem.package.metadata. Este nombre de archivo es especial para el sistema operativo y se lleva a cabo automáticamente durante las actualizaciones del sistema operativo. Los OEM pueden usar este archivo para pasar identificadores personalizados, de modo que las aplicaciones sepan cuándo los han implementado los OEM. Solo puede tener un archivo Custom.data por aplicación. Las aplicaciones deben poder buscar y leer este archivo correctamente. Los desarrolladores tratan el archivo como datos que no son de confianza.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Inicio rápido: Consulta de la información del manifiesto del paquete de aplicación](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Prerrequisitos

-   Necesita la herramienta [Administración y mantenimiento de imágenes de implementación (DISM) para](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) agregar el paquete de aplicación con el archivo de datos personalizado.

## <a name="instructions"></a>Instructions

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Paso 1: Crear un archivo personalizado y agregarlo a la carpeta de metadatos del paquete

Puede diseñar la aplicación para que use el formato que elija para los datos personalizados. Por ejemplo, puede usar XML, un archivo de texto u otro tipo de archivo para organizar los datos. Se recomienda tener en cuenta cómo puede probar y validar el archivo. Por ejemplo, puede crear un esquema XML para validar un archivo XML.

Puede especificar cualquier tipo de archivo con cualquier nombre de archivo para los datos personalizados. Al agregar el paquete de aplicación con el archivo de datos personalizado mediante la herramienta [DISM, DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) cambia el nombre del archivo personalizado a Custom.data y guarda el archivo en la carpeta tem.package.metadata de microsoft.sys.

> [!Note]  
> La aplicación no puede modificar el archivo de datos personalizado. Es un recurso de solo lectura.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Paso 2: Acceso al archivo de datos personalizado de una aplicación

Puede acceder al archivo Custom.data de una aplicación desde el código mediante Windows API para obtener información del paquete actual. Por ejemplo:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Para obtener más información sobre el desarrollo con la [**propiedad Package.Current,**](/uwp/api/windows.applicationmodel.package.current) vea Inicio rápido: Consulta de la información [del manifiesto del paquete de aplicación.](how-to-query-package-identity-information.md)

Para obtener más información sobre el acceso al archivo custom.data a través de [**IStorageFolder.GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) y el uso de objetos [**StorageFile,**](/uwp/api/Windows.Storage.StorageFile) consulte Acceso a [datos y archivos.](/previous-versions/windows/apps/hh464959(v=win.10))

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicio rápido: Consulta de la información del manifiesto del paquete de aplicación](how-to-query-package-identity-information.md)
</dt> </dl>

 

 