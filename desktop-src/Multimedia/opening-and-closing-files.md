---
title: Abrir y cerrar archivos
description: Abrir y cerrar archivos
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen función)
- AVIFileRelease función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689706"
---
# <a name="opening-and-closing-files"></a><span data-ttu-id="6d2ca-105">Abrir y cerrar archivos</span><span class="sxs-lookup"><span data-stu-id="6d2ca-105">Opening and Closing Files</span></span>

<span data-ttu-id="6d2ca-106">Una aplicación debe abrir un archivo AVI antes de leerlo o escribir en él.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-106">An application must open an AVI file before reading or writing.</span></span> <span data-ttu-id="6d2ca-107">Para abrir un archivo AVI, utilice la función [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) .</span><span class="sxs-lookup"><span data-stu-id="6d2ca-107">To open an AVI file, use the [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) function.</span></span> <span data-ttu-id="6d2ca-108">**AVIFileOpen** devuelve la dirección de una interfaz de archivo AVI que contiene el identificador del archivo abierto e incrementa el recuento de referencias del archivo.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-108">**AVIFileOpen** returns the address of an AVI file interface that contains the handle of the open file and increments the reference count of the file.</span></span>

<span data-ttu-id="6d2ca-109">La función **AVIFileOpen** admite el de las marcas usadas con la función [OpenFile](/documentation/) .</span><span class="sxs-lookup"><span data-stu-id="6d2ca-109">The **AVIFileOpen** function supports the OF flags used with the [OpenFile](/documentation/) function.</span></span> <span data-ttu-id="6d2ca-110">Si una aplicación escribe en un archivo existente, debe incluir el marcador de \_ escritura en **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-110">If an application writes to an existing file, it must include the OF\_WRITE flag in **AVIFileOpen**.</span></span> <span data-ttu-id="6d2ca-111">Del mismo modo, si la aplicación crea y escribe en un nuevo archivo, debe incluir la de \_ Create y de las \_ marcas de escritura en **AVIFileOpen**.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-111">Similarly, if your application creates and writes to a new file, you must include the OF\_CREATE and OF\_WRITE flags in **AVIFileOpen**.</span></span>

<span data-ttu-id="6d2ca-112">Al abrir un archivo con **AVIFileOpen**, puede utilizar un controlador de archivos predeterminado o puede especificar un controlador de archivos personalizado para leer y escribir en el archivo y sus flujos de datos.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-112">When you open a file using **AVIFileOpen**, you can use a default file handler or you can specify a custom file handler to read and write to the file and its data streams.</span></span> <span data-ttu-id="6d2ca-113">En cualquier caso, AVIFile busca en el registro el controlador de archivos correcto que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-113">In either case, AVIFile searches the registry for the correct file handler to use.</span></span> <span data-ttu-id="6d2ca-114">Debe asegurarse de que los controladores de archivos personalizados se encuentran en el registro antes de que una aplicación pueda tener acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-114">You must ensure custom file handlers are in the registry before an application can access them.</span></span>

<span data-ttu-id="6d2ca-115">Puede incrementar el recuento de referencias de un archivo mediante la función [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) .</span><span class="sxs-lookup"><span data-stu-id="6d2ca-115">You can increment the reference count of a file by using the [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) function.</span></span> <span data-ttu-id="6d2ca-116">Por ejemplo, puede que desee hacer esto al pasar un identificador de la interfaz de archivo a otra aplicación, o bien cuando desee mantener un archivo abierto mientras usa una función que normalmente cerraría el archivo.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-116">For example, you might want to do this when passing a handle of the file interface to another application, or when you want to keep a file open while using a function that would normally close the file.</span></span>

<span data-ttu-id="6d2ca-117">Puede cerrar un archivo mediante la función [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="6d2ca-117">You can close a file by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span> <span data-ttu-id="6d2ca-118">La función **AVIFileRelease** disminuye el recuento de referencias de un archivo AVI, guarda los cambios realizados en el archivo y, cuando el recuento de referencias llega a cero, cierra el archivo.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-118">The **AVIFileRelease** function decrements the reference count of an AVI file, saves changes made to the file, and when the reference count reaches zero, closes the file.</span></span> <span data-ttu-id="6d2ca-119">Las aplicaciones deben equilibrar el recuento de referencias incluyendo una llamada a **AVIFileRelease** para cada uso de [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) y **AVIFileAddRef**.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-119">Your applications should balance the reference count by including a call to **AVIFileRelease** for each use of [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) and **AVIFileAddRef**.</span></span>

> [!Note]  
> <span data-ttu-id="6d2ca-120">Una aplicación puede abrir un archivo con uno o más subprocesos del programa.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-120">An application can open a file with one or more program threads.</span></span> <span data-ttu-id="6d2ca-121">Sin embargo, para obtener el mejor rendimiento posible, solo un subproceso debe tener acceso al archivo en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="6d2ca-121">However, for the best possible performance, only one thread should access the file at any one time.</span></span>

 

 

 