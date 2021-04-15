---
title: Archivos de marcadores de posición
description: Archivos de marcadores de posición
ms.assetid: E14655DA-CEA0-4106-B882-C9E9116FC234
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c15037b0daec7a6521a299b6c4587c956e0be3
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "105665883"
---
# <a name="placeholder-files"></a>Archivos de marcadores de posición

## <a name="platform"></a>Plataforma

**Clientes-** Windows 8.1  
**Servidores:** Windows Server 2012 R2  

## <a name="description"></a>Descripción

Los archivos de marcadores de posición permiten a los usuarios ver y administrar archivos de OneDrive de Microsoft independientemente de la conectividad. Los archivos de marcadores de posición representan el espacio de nombres de OneDrive, incluso cuando los archivos no se almacenan en caché localmente. Contienen metadatos de archivo e imágenes en miniatura de las fotos.

## <a name="manifestation"></a>Manifestación

Para los usuarios finales y desarrolladores, los archivos de marcadores de posición tienen el mismo aspecto y comportamiento que los archivos locales.

Si la aplicación usa el cuadro de diálogo de archivo común para enumerar el sistema de archivos, la aplicación no se verá afectada. Cuando el usuario intente abrir el archivo desde el cuadro de diálogo común/File, se descargará el contenido del archivo y se pasará a la aplicación.

Si la aplicación accede directamente al sistema de archivos, la aplicación puede aprovechar los archivos de marcador de posición siguiendo las instrucciones que se indican a continuación.

## <a name="solution"></a>Solución

-   Los marcadores de posición están ocultos por Convención en función de los atributos
-   Identificar los marcadores de posición mediante el ID. de etiqueta de reanálisis e e/s volver a \_ analizar el \_ archivo de etiqueta \_ \_

Use el modelo de datos de Shell para un comportamiento sin problemas:

-   Usar SHCreateItemFromParsingName () para crear un elemento de Shell
-   Enlazar a la secuencia mediante IShellItem:: BindToHandler ( \_ secuencia BHID)
-   Controlador de propiedad de usuario para el acceso a propiedades (IShellItem2:: GetPropertyHandler)
-   Thumbnailhandler de Shell de usuario para obtener imágenes en miniatura de marcadores de posición
-   Especifique SupportedProtocols = \* en su implementación de verbo si el verbo se enlaza a la secuencia a través de BindToHandler


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



 

 




