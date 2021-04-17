---
description: La sección de instalación de un archivo INF define los pasos del procedimiento de instalación.
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: Ejemplo de sección de instalación de INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667998"
---
# <a name="inf-install-section-example"></a><span data-ttu-id="7e7ca-103">Ejemplo de sección de instalación de INF</span><span class="sxs-lookup"><span data-stu-id="7e7ca-103">INF Install Section Example</span></span>

<span data-ttu-id="7e7ca-104">La **sección de instalación de** un archivo INF define los pasos del procedimiento de instalación.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-104">The **Install** section of an INF File defines the steps of the installation procedure.</span></span> <span data-ttu-id="7e7ca-105">Cada línea de una sección de **instalación** tiene dos partes.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-105">Each line of an **Install** section has two parts.</span></span> <span data-ttu-id="7e7ca-106">A la izquierda del signo igual (=) es la clave.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-106">On the left of the equals sign (=) is the key.</span></span> <span data-ttu-id="7e7ca-107">En el lado derecho, es una lista de uno o varios títulos de sección.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-107">On the right hand side, is a list of one or more section titles.</span></span> <span data-ttu-id="7e7ca-108">La clave especifica el tipo de las secciones que se enumeran a la derecha.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-108">The key specifies the type of the sections that are listed on the right.</span></span> <span data-ttu-id="7e7ca-109">Para obtener una descripción del formato de esta sección, vea las secciones y directivas del archivo INF del kit de desarrollo de controladores de Microsoft Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-109">For a description of this section's format see the "INF File Sections and Directives" of the Microsoft Windows 2000 Driver Development Kit.</span></span>

<span data-ttu-id="7e7ca-110">El siguiente es un ejemplo de una sección de **instalación** .</span><span class="sxs-lookup"><span data-stu-id="7e7ca-110">The following is an example of an **Install** section.</span></span>

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

<span data-ttu-id="7e7ca-111">En este ejemplo, la clave **CopyFiles** se establece en los valores "files" y "ProgramFiles".</span><span class="sxs-lookup"><span data-stu-id="7e7ca-111">In this example the **CopyFiles** key is set to the values "DataFiles" and "ProgramFiles".</span></span> <span data-ttu-id="7e7ca-112">Esto especifica dos secciones **copiar archivos** en el archivo INF que contienen los nombres de los archivos de origen utilizados por las operaciones de copia.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-112">This specifies two **Copy Files** sections in the INF file that contain the names of the source files used by copying operations.</span></span> <span data-ttu-id="7e7ca-113">El destino de los archivos copiados se especificaría en una sección **DestinationDirs** del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-113">The destination for the copied files would be specified in a **DestinationDirs** section in the INF file.</span></span>

<span data-ttu-id="7e7ca-114">A la clave **Delfiles** se le asigna el valor "OldFiles".</span><span class="sxs-lookup"><span data-stu-id="7e7ca-114">The **Delfiles** key is given the value "OldFiles".</span></span> <span data-ttu-id="7e7ca-115">Esto especifica una sección **eliminar archivos** que contiene información pertinente para las operaciones de eliminación de archivos.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-115">This specifies a **Delete Files** section that contains information relevant to file deletion operations.</span></span>

<span data-ttu-id="7e7ca-116">La clave **UpdateInis** especifica las secciones **Update ini File** que contienen información sobre la actualización de entradas en el archivo ini.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-116">The **UpdateInis** key specifies **Update INI File** sections that contain information about updating entries in the INI file.</span></span>

<span data-ttu-id="7e7ca-117">Las claves **AddReg** y **DelReg** especifican las secciones **Agregar registro** y **Eliminar registro** que contienen información acerca de cómo agregar o eliminar información del registro.</span><span class="sxs-lookup"><span data-stu-id="7e7ca-117">The **AddReg** and **DelReg** keys specify **Add Registry** and **Delete Registry** sections that contain information about adding or deleting registry information.</span></span>

 

 



