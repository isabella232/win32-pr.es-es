---
title: Cómo desarrollar una aplicación de OEM que use un archivo personalizado
description: Obtenga información sobre cómo desarrollar una aplicación que use un archivo personalizado para pasar información del OEM a la aplicación.
ms.assetid: BCDB4B13-3644-44E4-9A70-04D8E90500EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cf60364138a80317e6db8ac4c5d028c36ff540f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105704933"
---
# <a name="how-to-develop-an-oem-app-that-uses-a-custom-file"></a>Cómo desarrollar una aplicación de OEM que use un archivo personalizado

Para obtener más información sobre la creación y el uso de archivos de datos personalizados, consulte [Opciones de mantenimiento del paquete de aplicación de DISM (. appx o. appxbundle) Command-Line](/windows-hardware/manufacture/desktop/dism-app-package--appx-or-appxbundle--servicing-command-line-options).

Obtenga información sobre cómo desarrollar una aplicación que use un archivo personalizado para pasar información del OEM a la aplicación.

En el caso de las aplicaciones que cree para la implementación de OEM, puede usar un archivo personalizado para pasar información del OEM a las aplicaciones. Para pasar información de OEM a una aplicación, cree un archivo. Data personalizado en la carpeta microsoft.sysTEM. Package. Metadata. Este nombre de archivo es especial para el sistema operativo y se realiza automáticamente durante las actualizaciones del sistema operativo. Los OEM pueden usar este archivo para pasar identificadores personalizados, de modo que las aplicaciones sepan cuándo han implementado los OEM. Solo puede tener un archivo. Data personalizado por aplicación. Las aplicaciones deben poder buscar y leer este archivo correctamente. Los desarrolladores tratan el archivo como datos que no son de confianza.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Inicio rápido: información del manifiesto del paquete de la aplicación de consulta](how-to-query-package-identity-information.md)

### <a name="prerequisites"></a>Requisitos previos

-   Necesita la herramienta [Administración y mantenimiento de imágenes de implementación (DISM)](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) para agregar el paquete de la aplicación con el archivo de datos personalizado.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-create-custom-file-and-add-it-to-the-package-metadata-folder"></a>Paso 1: crear un archivo personalizado y agregarlo a la carpeta de metadatos del paquete

Puede diseñar la aplicación para que use cualquier formato que elija para los datos personalizados. Por ejemplo, puede usar XML, un archivo de texto u otro tipo de archivo para organizar los datos. Le recomendamos que considere cómo puede probar y validar el archivo. Por ejemplo, puede crear un esquema XML para validar un archivo XML.

Puede especificar cualquier tipo de archivo con cualquier nombre de archivo para los datos personalizados. Al agregar el paquete de la aplicación con el archivo de datos personalizado mediante la herramienta [DISM](/windows/desktop/Win7AppQual/dism-replaces-pkgmgr-peimg-and-intlconfg-tools) , DISM cambia el nombre del archivo personalizado a Custom. Data y guarda el archivo en la carpeta microsoft.sysTEM. Package. Metadata.

> [!Note]  
> La aplicación no puede modificar el archivo de datos personalizado. Es un recurso de solo lectura.

 

### <a name="step-2-access-the-custom-data-file-for-an-app"></a>Paso 2: acceder al archivo de datos personalizado para una aplicación

Puede tener acceso al archivo. Data personalizado para una aplicación desde el código mediante las API de Windows para obtener información del paquete actual. Por ejemplo:

``` syntax
Windows.ApplicationModel.Package.current.installedLocation.getFileAsync(
"microsoft.system.package.metadata\\custom.data")
```

Para obtener más información sobre el desarrollo con la propiedad [**Package. Current**](/uwp/api/windows.applicationmodel.package.current) , consulte [Inicio rápido: información del manifiesto del paquete](how-to-query-package-identity-information.md)de la aplicación de consulta.

Para obtener más información sobre el acceso al archivo. Data personalizado a través de [**IStorageFolder. GetFileAsync**](/uwp/api/windows.storage.istoragefolder.getfileasync) y el uso de objetos [**StorageFile**](/uwp/api/Windows.Storage.StorageFile) , vea [acceso a datos y archivos](/previous-versions/windows/apps/hh464959(v=win.10)).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Inicio rápido: información del manifiesto del paquete de la aplicación de consulta](how-to-query-package-identity-information.md)
</dt> </dl>

 

 