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
# <a name="placeholder-files"></a><span data-ttu-id="24b54-103">Archivos de marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="24b54-103">Placeholder files</span></span>

## <a name="platform"></a><span data-ttu-id="24b54-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="24b54-104">Platform</span></span>

<span data-ttu-id="24b54-105">**Clientes-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="24b54-105">**Clients -** Windows 8.1</span></span>  
<span data-ttu-id="24b54-106">**Servidores:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="24b54-106">**Servers -** Windows Server 2012 R2</span></span>  

## <a name="description"></a><span data-ttu-id="24b54-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="24b54-107">Description</span></span>

<span data-ttu-id="24b54-108">Los archivos de marcadores de posición permiten a los usuarios ver y administrar archivos de OneDrive de Microsoft independientemente de la conectividad.</span><span class="sxs-lookup"><span data-stu-id="24b54-108">Placeholder files enable users to view and manage Microsoft OneDrive files regardless of connectivity.</span></span> <span data-ttu-id="24b54-109">Los archivos de marcadores de posición representan el espacio de nombres de OneDrive, incluso cuando los archivos no se almacenan en caché localmente.</span><span class="sxs-lookup"><span data-stu-id="24b54-109">Placeholder files represent the OneDrive namespace, even when files are not cached locally.</span></span> <span data-ttu-id="24b54-110">Contienen metadatos de archivo e imágenes en miniatura de las fotos.</span><span class="sxs-lookup"><span data-stu-id="24b54-110">They contain file metadata and thumbnail images of photos.</span></span>

## <a name="manifestation"></a><span data-ttu-id="24b54-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="24b54-111">Manifestation</span></span>

<span data-ttu-id="24b54-112">Para los usuarios finales y desarrolladores, los archivos de marcadores de posición tienen el mismo aspecto y comportamiento que los archivos locales.</span><span class="sxs-lookup"><span data-stu-id="24b54-112">To end users and developers, placeholder files look and behave almost the same as the local files.</span></span>

<span data-ttu-id="24b54-113">Si la aplicación usa el cuadro de diálogo de archivo común para enumerar el sistema de archivos, la aplicación no se verá afectada.</span><span class="sxs-lookup"><span data-stu-id="24b54-113">If your app uses the Common File Dialog to enumerate the file system, your app will not be impacted.</span></span> <span data-ttu-id="24b54-114">Cuando el usuario intente abrir el archivo desde el cuadro de diálogo común/File, se descargará el contenido del archivo y se pasará a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24b54-114">When the user tries to open the file from the common /file Dialog, the file content will be downloaded and will be passed to your app.</span></span>

<span data-ttu-id="24b54-115">Si la aplicación accede directamente al sistema de archivos, la aplicación puede aprovechar los archivos de marcador de posición siguiendo las instrucciones que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="24b54-115">If your app accesses the file system directly, then your app may take advantage of the placeholder files by using the guidelines below.</span></span>

## <a name="solution"></a><span data-ttu-id="24b54-116">Solución</span><span class="sxs-lookup"><span data-stu-id="24b54-116">Solution</span></span>

-   <span data-ttu-id="24b54-117">Los marcadores de posición están ocultos por Convención en función de los atributos</span><span class="sxs-lookup"><span data-stu-id="24b54-117">Placeholders are hidden by convention based on attributes</span></span>
-   <span data-ttu-id="24b54-118">Identificar los marcadores de posición mediante el ID. de etiqueta de reanálisis e e/s volver a \_ analizar el \_ archivo de etiqueta \_ \_</span><span class="sxs-lookup"><span data-stu-id="24b54-118">Identify placeholders using reparse tag ID IO\_REPARSE\_TAG\_FILE\_PLACEHOLDER</span></span>

<span data-ttu-id="24b54-119">Use el modelo de datos de Shell para un comportamiento sin problemas:</span><span class="sxs-lookup"><span data-stu-id="24b54-119">Use the shell data model for seamless behavior:</span></span>

-   <span data-ttu-id="24b54-120">Usar SHCreateItemFromParsingName () para crear un elemento de Shell</span><span class="sxs-lookup"><span data-stu-id="24b54-120">Use SHCreateItemFromParsingName() to create a shell item</span></span>
-   <span data-ttu-id="24b54-121">Enlazar a la secuencia mediante IShellItem:: BindToHandler ( \_ secuencia BHID)</span><span class="sxs-lookup"><span data-stu-id="24b54-121">Bind to the stream using IShellItem::BindToHandler(BHID\_Stream)</span></span>
-   <span data-ttu-id="24b54-122">Controlador de propiedad de usuario para el acceso a propiedades (IShellItem2:: GetPropertyHandler)</span><span class="sxs-lookup"><span data-stu-id="24b54-122">User property handler for property access (IShellItem2::GetPropertyHandler)</span></span>
-   <span data-ttu-id="24b54-123">Thumbnailhandler de Shell de usuario para obtener imágenes en miniatura de marcadores de posición</span><span class="sxs-lookup"><span data-stu-id="24b54-123">User shell thumbnailhandler to get thumbnail images for placeholders</span></span>
-   <span data-ttu-id="24b54-124">Especifique SupportedProtocols = \* en su implementación de verbo si el verbo se enlaza a la secuencia a través de BindToHandler</span><span class="sxs-lookup"><span data-stu-id="24b54-124">Specify SupportedProtocols=\* on your verb implementation if the verb binds to the stream via BindToHandler</span></span>


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



 

 




