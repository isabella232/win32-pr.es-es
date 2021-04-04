---
title: Los archivos de Common-Store y el almacén común de SIS
description: Todos los archivos de copia de seguridad mantenidos por la copia de seguridad del almacén de instancia única (SIS) se denominan archivos de almacenamiento común.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Copias de seguridad de almacenes comunes
- Copia de seguridad de almacenamiento de instancia única (SIS), almacenes comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904726"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="58321-105">Los archivos de Common-Store y el almacén común de SIS</span><span class="sxs-lookup"><span data-stu-id="58321-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="58321-106">Todos los archivos de copia de seguridad mantenidos por la copia de seguridad del almacén de instancia única (SIS) se denominan *archivos de almacenamiento común*.</span><span class="sxs-lookup"><span data-stu-id="58321-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="58321-107">Existe un *almacén común* en cada volumen de mantenidos por sis y contiene todos los archivos de almacenamiento común que existen en ese volumen.</span><span class="sxs-lookup"><span data-stu-id="58321-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="58321-108">Este directorio se encuentra en el directorio raíz del volumen y se denomina " \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="58321-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="58321-109">Common Store se implementa como un directorio protegido contra el acceso de usuario normal, ya que los archivos de almacenamiento común están pensados para que solo los puedan acceder directamente a las funciones de la API de copia de seguridad de SIS y no a las aplicaciones de copia de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="58321-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="58321-110">Las propiedades de un archivo de almacenamiento común son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="58321-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="58321-111">Un archivo de almacenamiento común puede tener uno o varios vínculos que señalen a él.</span><span class="sxs-lookup"><span data-stu-id="58321-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="58321-112">Una vez creado, el contenido de un archivo de almacenamiento común nunca cambia.</span><span class="sxs-lookup"><span data-stu-id="58321-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="58321-113">Los nombres de los archivos de almacenamiento común son únicos globalmente, es decir, son únicos en todos los volúmenes en todos los sistemas del mundo, y el enlace entre un nombre de archivo de almacenamiento común y sus datos es globalmente estático.</span><span class="sxs-lookup"><span data-stu-id="58321-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="58321-114">Cuando SIS está habilitado en un volumen, se crea una copia de los archivos duplicados en el almacén común y todos los archivos duplicados se reemplazan por [vínculos de SIS](sis-links-and-reparse-points.md) que señalan al archivo de almacenamiento común.</span><span class="sxs-lookup"><span data-stu-id="58321-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="58321-115">Para obtener más información, consulte [habilitar o deshabilitar SIS en un volumen](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) en la documentación de TechNet.</span><span class="sxs-lookup"><span data-stu-id="58321-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="58321-116">Cuando se tiene acceso a uno de los vínculos SIS para una operación de escritura, el filtro SIS restaura primero el contenido original del archivo de vínculo SIS del archivo Common-Store, se quita el punto de reanálisis que vincula el archivo de vínculo SIS al almacén común y, a continuación, se realiza la operación de escritura en el archivo de destino original.</span><span class="sxs-lookup"><span data-stu-id="58321-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="58321-117">El archivo Common-Store se quita solo cuando se elimina el último vínculo SIS que apunta a él.</span><span class="sxs-lookup"><span data-stu-id="58321-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 