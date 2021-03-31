---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La biblioteca de archivos reemplaza a la carpeta de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912758"
---
# <a name="file-library-replaces-document-folder"></a>La biblioteca de archivos reemplaza a la carpeta de documentos

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes** : Windows 7  
**Servidores** : Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad** : medio  
**Frecuencia** : alta  











## <a name="description"></a>Descripción

Las bibliotecas proporcionan una experiencia de tipo carpeta centralizada para el almacenamiento de archivos, la búsqueda y el acceso a través de varias ubicaciones, tanto locales como remotas.

Las ubicaciones predeterminadas que usan los cuadros de diálogo de archivos comunes (por ejemplo, abrir y guardar) se han cambiado de la carpeta de documentos a la biblioteca de documentos. La interfaz de usuario no ha cambiado, pero el usuario podrá ver, examinar y buscar en la biblioteca mediante varias vistas de organización. Los archivos se guardarán en la ubicación de almacenamiento predeterminada de la biblioteca, a menos que el usuario cambie la ubicación de almacenamiento predeterminada o elija otra carpeta.

Los desarrolladores pueden crear sus propias bibliotecas o agregar ubicaciones a las bibliotecas existentes mediante la interfaz IShellLibrary. Los usuarios pueden encontrar bibliotecas mediante el sistema de carpetas conocido (por ejemplo, FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Manifiesto de impacto

La biblioteca es un archivo, no una carpeta. Por lo tanto, las manipulaciones de ruta de acceso podrían producir errores debido al intento de la aplicación de concatenar archivos en los archivos.

## <a name="solution"></a>Solución

Al usar IFileDialog, debe usar el método GetResult en lugar de la combinación de GetFolder y GetFilename, tal como lo haría en las versiones anteriores del sistema operativo. Use las API de Shell donde sea posible para interactuar con los elementos del espacio de nombres del shell y manipularlos (por ejemplo, IShellItem).

## <a name="leveraging-feature-capabilities"></a>Aprovechar las capacidades de características

Si desea crear sus propias bibliotecas o agregar ubicaciones a las bibliotecas existentes, debe usar la API de IShellLibrary. Las bibliotecas son carpetas de Shell, por lo que puede enumerarlas como cualquier otra carpeta de Shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

Al usar el cuadro de diálogo archivo común, se asegurará de que los usuarios pueden guardar directamente en sus bibliotecas.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   **Bibliotecas de Windows:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantener la sincronización con una biblioteca:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



