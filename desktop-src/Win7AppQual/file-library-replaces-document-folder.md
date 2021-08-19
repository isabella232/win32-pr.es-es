---
description: La biblioteca de archivos reemplaza la carpeta de documentos
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: La biblioteca de archivos reemplaza la carpeta de documentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e8d08b176ebf4b5801a73695ea03f60a38eeb5a1ca51e1d90d9119dae5fcaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329675"
---
# <a name="file-library-replaces-document-folder"></a>La biblioteca de archivos reemplaza la carpeta de documentos

## <a name="affected-platforms"></a>Plataformas afectadas

**Clientes:** Windows 7  
**Servidores:** Windows Server 2008 R2  









## <a name="feature-impact"></a>Impacto en las características

**Gravedad:** media  
**Frecuencia:** alta  











## <a name="description"></a>Descripción

Las bibliotecas proporcionan una experiencia centralizada de tipo carpeta para el almacenamiento de archivos, la búsqueda y el acceso en varias ubicaciones, tanto locales como remotas.

Las ubicaciones predeterminadas que usan los cuadros de diálogo de archivos comunes (por ejemplo, Abrir y Guardar) se han cambiado de la carpeta de documentos a la biblioteca de documentos. El Interfaz de usuario no ha cambiado, pero el usuario ahora podrá ver, examinar y buscar en la biblioteca mediante varias vistas de organización. Los archivos se guardarán en la ubicación de guardado predeterminada de la biblioteca a menos que el usuario cambie la ubicación de guardado predeterminada o elija otra carpeta.

Los desarrolladores podrían crear sus propias bibliotecas o agregar ubicaciones a las bibliotecas existentes mediante la interfaz IShellLibrary. Los usuarios pueden encontrar bibliotecas mediante el sistema de carpetas conocidas (por ejemplo, FOLDERID \_ DocumentsLibrary).

## <a name="manifestation-of-impact"></a>Demostración de impacto

La biblioteca es en sí misma un archivo y no una carpeta. Por lo tanto, las manipulaciones de ruta de acceso podrían producir errores debido al intento de la aplicación de concatenar archivos a archivos.

## <a name="solution"></a>Solución

Al usar IFileDialog, debe usar el método GetResult en lugar de la combinación de GetFolder y GetFilename como lo haría en las versiones anteriores del sistema operativo. Use las API de Shell siempre que sea posible para interactuar y manipular elementos en el espacio de nombres de Shell (por ejemplo, IShellItem).

## <a name="leveraging-feature-capabilities"></a>Aprovechamiento de las funcionalidades de características

Si desea crear sus propias bibliotecas o agregar ubicaciones a las bibliotecas existentes, debe usar IShellLibrary API. Las bibliotecas son carpetas de shell, por lo que puede enumerarlos como cualquier otra carpeta de shell.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso

El uso del cuadro de diálogo de archivo común garantizará que los usuarios puedan guardar directamente en sus bibliotecas.

## <a name="links-to-other-resources"></a>Vínculos a otros recursos

-   **Windows bibliotecas:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx
-   **Mantener la sincronización con una biblioteca:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync

 

 



