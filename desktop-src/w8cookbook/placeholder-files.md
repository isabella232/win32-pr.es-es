---
title: Archivos de marcador de posición
description: Archivos de marcador de posición
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127262375"
---
# <a name="placeholder-files"></a>Archivos de marcador de posición

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8.1  
**Servidores:** Windows Server 2012 R2  

## <a name="description"></a>Descripción

Los archivos de marcador de posición permiten a los usuarios ver y administrar Microsoft OneDrive archivos, independientemente de la conectividad. Los archivos de marcador de posición representan OneDrive espacio de nombres, incluso cuando los archivos no se almacenan en caché localmente. Contienen metadatos de archivo e imágenes en miniatura de fotos.

## <a name="manifestation"></a>Manifestación

Para los usuarios finales y desarrolladores, los archivos de marcador de posición parecen y se comportan casi igual que los archivos locales.

Si la aplicación usa el cuadro de diálogo Archivo común para enumerar el sistema de archivos, la aplicación no se verá afectada. Cuando el usuario intente abrir el archivo desde el cuadro de diálogo /file común, el contenido del archivo se descargará y se pasará a la aplicación.

Si la aplicación accede directamente al sistema de archivos, la aplicación puede aprovechar los archivos de marcador de posición mediante las instrucciones siguientes.

## <a name="solution"></a>Solución

-   Los marcadores de posición se ocultan por convención en función de los atributos
-   Identificación de marcadores de posición mediante id. de etiqueta de reantiqueta \_ E/S REPARSE \_ TAG FILE \_ \_ PLACEHOLDER

Use el modelo de datos de shell para un comportamiento sin problemas:

-   Uso de SHCreateItemFromParsingName() para crear un elemento de shell
-   Enlazar a la secuencia mediante IShellItem::BindToHandler(STREAM \_ DESUSDAID)
-   Controlador de propiedades de usuario para el acceso a propiedades (IShellItem2::GetPropertyHandler)
-   ThumbnailHandler del shell de usuario para obtener imágenes en miniatura para marcadores de posición
-   Especifique SupportedProtocols= en la implementación del verbo si el verbo se enlaza \* a la secuencia a través de BindToHandler.


```
#include <winnth> //for IO_REPARSE_TAG_FILE_PLACEHOLDER
//  Helper that indicates this is a 
bool IsFilePlaceholder(WIN32_FIND_DATA const &findData)
{
  return (findData.dwFileAttributes & FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
}
bool IsFilePlaceholder(_In_PCWSTR filePath)
{
  bool isPlaceholder = false;
  WIN32_FIND_DATA findData;
  HANDLE hFind = FindFirstFile(filePath, &findData);
  if (hFind ! = INVALID_HANDLE_VALUE)
  {
    isPlaceholder = (findData.dwFileAttributes &    FILE_ATTRIBUTE_REPARSE_POINT) &&
    (findData.dwReserved0 == IO_REPARSE_TAG_FILE_PLACEHOLDER);
    FindClose(hFind);
  }
  Return isPlaceholder;
}
```



 

 




