---
title: archivos compuestos
description: Aunque puede implementar sus propios objetos e interfaces de almacenamiento estructurado, COM proporciona una implementación estándar denominada archivos compuestos.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268390"
---
# <a name="compound-files"></a><span data-ttu-id="5bcc9-103">archivos compuestos</span><span class="sxs-lookup"><span data-stu-id="5bcc9-103">Compound Files</span></span>

<span data-ttu-id="5bcc9-104">Aunque puede implementar sus propios objetos e interfaces de almacenamiento estructurado, COM proporciona una implementación estándar denominada archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-104">Although you can implement your own structured storage objects and interfaces, COM provides a standard implementation called Compound Files.</span></span> <span data-ttu-id="5bcc9-105">El uso de archivos compuestos le permite guardar el trabajo de codificación de su propia implementación de almacenamiento estructurado y confiere varias ventajas adicionales derivadas de la adhesión a un estándar definido.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-105">Using Compound Files saves you the work of coding your own implementation of structured storage and confers several additional benefits derived from adhering to a defined standard.</span></span> <span data-ttu-id="5bcc9-106">Entre estos beneficios, se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5bcc9-106">These benefits include the following:</span></span>

-   <span data-ttu-id="5bcc9-107">**Independencia del sistema de archivos y la plataforma**.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-107">**File-system and platform independence**.</span></span> <span data-ttu-id="5bcc9-108">Dado que la implementación de archivos compuestos de COM se ejecuta sobre sistemas de archivos sin formato existentes, las aplicaciones pueden abrir los archivos compuestos almacenados en el sistema de archivos FAT, en el sistema de archivos NTFS o en los sistemas de archivos de Macintosh con cualquiera de los demás sistemas de archivos.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-108">Because COM's Compound Files implementation runs on top of existing flat-file systems, compound files stored in the FAT file system, NTFS file system, or Macintosh file systems can be opened by applications using any one of the other file systems.</span></span>
-   <span data-ttu-id="5bcc9-109">**Búsqueda**.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-109">**Searchable**.</span></span> <span data-ttu-id="5bcc9-110">Dado que los objetos independientes de un archivo compuesto se guardan en un formato estándar y se puede tener acceso a ellos mediante interfaces y API COM estándar, cualquier utilidad del explorador que use estas interfaces y API puede enumerar los objetos del archivo, aunque los datos de un objeto determinado pueden estar en un formato de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-110">Because the separate objects in a compound file are saved in a standard format and can be accessed using standard COM interfaces and APIs, any browser utility using these interfaces and APIs can list the objects in the file, even though data within a given object may be in a proprietary format.</span></span>
-   <span data-ttu-id="5bcc9-111">**Acceso a determinados datos internos**.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-111">**Access to certain internal data**.</span></span> <span data-ttu-id="5bcc9-112">Dado que la implementación de archivos compuestos proporciona formas estándar de escribir determinados tipos de datos (información de Resumen, por ejemplo), las aplicaciones pueden leer estos datos mediante interfaces y API COM.</span><span class="sxs-lookup"><span data-stu-id="5bcc9-112">Because the Compound Files implementation provides standard ways of writing certain types of data—summary information, for example—applications can read this data using COM interfaces and APIs.</span></span>

 

 




