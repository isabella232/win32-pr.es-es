---
description: Un contenedor es un archivo único, normalmente con una extensión. cab, que almacena los archivos comprimidos en una biblioteca de archivos.
ms.assetid: df240302-b875-49bf-8e62-7a35204c35fb
title: Archivos. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b54ae737785abc33edd46c9e53edc93fcd288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667009"
---
# <a name="cabinet-files"></a><span data-ttu-id="f7516-103">Archivos. cab</span><span class="sxs-lookup"><span data-stu-id="f7516-103">Cabinet Files</span></span>

<span data-ttu-id="f7516-104">Un contenedor es un archivo único, normalmente con una extensión. cab, que almacena los archivos comprimidos en una biblioteca de archivos.</span><span class="sxs-lookup"><span data-stu-id="f7516-104">A cabinet is a single file, usually with a .cab extension, that stores compressed files in a file library.</span></span> <span data-ttu-id="f7516-105">El formato de archivo. cab es una manera eficaz de empaquetar varios archivos, ya que la compresión se realiza a través de los límites de los archivos, lo que mejora significativamente la razón de compresión.</span><span class="sxs-lookup"><span data-stu-id="f7516-105">The cabinet format is an efficient way to package multiple files because compression is performed across file boundaries, which significantly improves the compression ratio.</span></span>

<span data-ttu-id="f7516-106">Los desarrolladores pueden usar una herramienta de creación de archivos. cab como Makecab.exe para crear archivos. cab para su uso con paquetes de instalador.</span><span class="sxs-lookup"><span data-stu-id="f7516-106">Developers can use a cabinet file creation tool such as Makecab.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="f7516-107">La utilidad de Makecab.exe se incluye en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="f7516-107">The Makecab.exe utility is included in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="f7516-108">Los desarrolladores también pueden utilizar una herramienta de creación de archivos. cab como Cabarc.exe para crear archivos. cab para su uso con paquetes de instalador.</span><span class="sxs-lookup"><span data-stu-id="f7516-108">Developers can also use a cabinet file creation tool such as Cabarc.exe to make cabinet files for use with installer packages.</span></span> <span data-ttu-id="f7516-109">Esta herramienta escribe en la estructura del archivo. cab de Diamond.</span><span class="sxs-lookup"><span data-stu-id="f7516-109">This tool writes to the Diamond cabinet structure.</span></span>

<span data-ttu-id="f7516-110">Las claves de archivo de los archivos almacenados dentro de un archivo. cab deben coincidir con las entradas de la columna File de la [tabla File](file-table.md) y la secuencia de archivos del archivo. cab debe coincidir con la secuencia de archivos especificada en la columna Sequence.</span><span class="sxs-lookup"><span data-stu-id="f7516-110">The file keys of the files stored inside of a cabinet file must match the entries in the File column of the [File table](file-table.md) and the sequence of files in the cabinet must match the file sequence specified in the Sequence column.</span></span> <span data-ttu-id="f7516-111">Para obtener más información, consulte [uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="f7516-111">For more information, see [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="f7516-112">Los archivos grandes pueden dividirse entre dos o más archivos. cab.</span><span class="sxs-lookup"><span data-stu-id="f7516-112">Large files can be split between two or more cabinet files.</span></span> <span data-ttu-id="f7516-113">No puede haber más de 15 archivos en un archivo contenedor que abarque al siguiente archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="f7516-113">There can be no more than 15 files in any one cabinet file that spans to the next cabinet file.</span></span> <span data-ttu-id="f7516-114">Por ejemplo, si tiene tres archivos. cab, el primero puede tener 15 archivos que abarcan el segundo archivo. cab y el segundo archivo. cab puede tener 15 archivos que abarcan el tercer archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="f7516-114">For example, if you have three cabinet files the first cabinet can have 15 files that span to the second cabinet file and the second cabinet file can have 15 files that span to the third cabinet file.</span></span>

<span data-ttu-id="f7516-115">El instalador extrae los archivos de un archivo. cab, ya que los necesita la instalación y los instala en el mismo orden en el que se almacenan en el archivo. cab.</span><span class="sxs-lookup"><span data-stu-id="f7516-115">The installer extracts files from a cabinet as they are needed by the installation and installs them in the same order as they are stored in the cabinet file.</span></span> <span data-ttu-id="f7516-116">Los requisitos de espacio para instalar un archivo almacenado en un archivo. cab no son diferentes a los de la instalación de un archivo sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="f7516-116">The space requirements for installing a file stored in a cabinet are no different than for installing an uncompressed file.</span></span>

<span data-ttu-id="f7516-117">Un archivo. cab se puede ubicar dentro o fuera del archivo. msi.</span><span class="sxs-lookup"><span data-stu-id="f7516-117">A cabinet file can be located inside or outside of the .msi file.</span></span> <span data-ttu-id="f7516-118">A partir de Windows Installer 5,0 que se ejecuta en Windows 7 o Windows Server 2008 R2, el instalador guarda los archivadores que están incrustados en el archivo. msi antes de almacenar en caché el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="f7516-118">Beginning with Windows Installer 5.0 running on Windows 7 or Windows Server 2008 R2 the installer saves any cabinets that are embedded in the .msi file before caching the installation package.</span></span>

<span data-ttu-id="f7516-119">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** Para conservar espacio en disco, el instalador siempre quita todos los gabinetes que están incrustados en el archivo. msi antes de almacenar en caché el paquete de instalación en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f7516-119">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** To conserve disk space, the installer always removes any cabinets that are embedded in the .msi file before caching the installation package on the user's computer.</span></span>

 

 



