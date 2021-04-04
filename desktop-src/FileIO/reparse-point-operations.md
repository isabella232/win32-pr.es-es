---
description: Describe las operaciones de punto de reanálisis que se pueden realizar mediante DeviceIoControl.
ms.assetid: c7279203-2443-401e-b541-038954094266
title: Operaciones de punto de análisis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0889120af50c8415ed255b8274b76f2d53e6a563
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083160"
---
# <a name="reparse-point-operations"></a><span data-ttu-id="9856b-103">Operaciones de punto de análisis</span><span class="sxs-lookup"><span data-stu-id="9856b-103">Reparse Point Operations</span></span>

<span data-ttu-id="9856b-104">Para determinar si un sistema de archivos admite puntos de análisis, llame a la función [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) y examine el archivo compatible con la marca de bits **\_ \_ \_ puntos de reanálisis** .</span><span class="sxs-lookup"><span data-stu-id="9856b-104">To determine whether a file system supports reparse points, call the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examine the **FILE\_SUPPORTS\_REPARSE\_POINTS** bit flag.</span></span>

<span data-ttu-id="9856b-105">La función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) permite establecer, modificar, obtener y quitar puntos de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="9856b-105">The [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables you to set, modify, obtain, and remove reparse points.</span></span> <span data-ttu-id="9856b-106">En la tabla siguiente se describen las operaciones de punto de reanálisis que se pueden realizar con **DeviceIoControl**.</span><span class="sxs-lookup"><span data-stu-id="9856b-106">The following table describes the reparse point operations that you can perform using **DeviceIoControl**.</span></span>



| <span data-ttu-id="9856b-107">Operación</span><span class="sxs-lookup"><span data-stu-id="9856b-107">Operation</span></span>                                                           | <span data-ttu-id="9856b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9856b-108">Description</span></span>                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9856b-109">**\_grupo de \_ análisis de conjunto de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="9856b-109">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)       | <span data-ttu-id="9856b-110">Permite al programa que realiza la llamada establecer un nuevo punto de análisis o modificar uno existente.</span><span class="sxs-lookup"><span data-stu-id="9856b-110">Allows the calling program to set a new reparse point, or to modify an existing one.</span></span><br/> |
| [<span data-ttu-id="9856b-111">**\_punto de \_ repetición de análisis de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="9856b-111">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)       | <span data-ttu-id="9856b-112">Obtiene la información almacenada en un punto de reanálisis existente.</span><span class="sxs-lookup"><span data-stu-id="9856b-112">Obtains the information stored in an existing reparse point.</span></span><br/>                         |
| [<span data-ttu-id="9856b-113">**\_punto de \_ reanálisis de eliminación de FSCTL \_**</span><span class="sxs-lookup"><span data-stu-id="9856b-113">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point) | <span data-ttu-id="9856b-114">Quita un punto de reanálisis existente.</span><span class="sxs-lookup"><span data-stu-id="9856b-114">Removes an existing reparse point.</span></span><br/>                                                   |



 

<span data-ttu-id="9856b-115">Si va a modificar, obtener o eliminar un punto de repetición de análisis, debe especificar la misma etiqueta de reanálisis en la operación incluida en el archivo.</span><span class="sxs-lookup"><span data-stu-id="9856b-115">If you are modifying, getting, or deleting a reparse point, you must specify the same reparse tag in the operation that is contained in the file.</span></span> <span data-ttu-id="9856b-116">De lo contrario, se producirá un error en la operación y la **etiqueta de REanálisis de errores de error \_ \_ \_ no coincide**.</span><span class="sxs-lookup"><span data-stu-id="9856b-116">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_TAG\_MISMATCH**.</span></span> <span data-ttu-id="9856b-117">Si va a modificar o eliminar un punto de repetición de análisis, también debe especificar el **GUID** de reanálisis en la operación contenida en el archivo.</span><span class="sxs-lookup"><span data-stu-id="9856b-117">If you are modifying or deleting a reparse point, you must also specify the reparse **GUID** in the operation that is contained in the file.</span></span> <span data-ttu-id="9856b-118">De lo contrario, se producirá un error en la operación con el **\_ conflicto de \_ atributos \_ de reanálisis de errores**.</span><span class="sxs-lookup"><span data-stu-id="9856b-118">Otherwise, the operation will fail with the error **ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**.</span></span>

<span data-ttu-id="9856b-119">Para determinar si un archivo o directorio contiene un punto de reanálisis, utilice la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) .</span><span class="sxs-lookup"><span data-stu-id="9856b-119">To determine whether a file or directory contains a reparse point, use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function.</span></span> <span data-ttu-id="9856b-120">Si el archivo o el directorio tiene un punto de análisis asociado, se establece el atributo de **\_ \_ \_ punto de reanálisis del atributo de archivo** .</span><span class="sxs-lookup"><span data-stu-id="9856b-120">If the file or directory has an associated reparse point, the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute is set.</span></span>

<span data-ttu-id="9856b-121">Para sobrescribir un punto de reanálisis existente sin tener ya un identificador para el archivo o directorio, llame a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con el **marcador de archivo abrir el \_ \_ \_ \_ punto de reanálisis**.</span><span class="sxs-lookup"><span data-stu-id="9856b-121">To overwrite an existing reparse point without already having a handle to the file or directory, call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) with **FILE\_FLAG\_OPEN\_REPARSE\_POINT**.</span></span> <span data-ttu-id="9856b-122">Esta marca permite abrir el archivo independientemente de si el filtro del sistema de archivos correspondiente está instalado y funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="9856b-122">This flag allows you to open the file whether or not the corresponding file system filter is installed and working correctly.</span></span>

 

