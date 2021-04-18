---
description: Puede almacenar cualquier tipo de datos específicos de la aplicación con una superficie. Por ejemplo, una superficie que representa un mapa en un juego podría contener información sobre el terreno.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Datos de la superficie privada (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714779"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="a36ce-104">Datos de la superficie privada (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a36ce-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="a36ce-105">Puede almacenar cualquier tipo de datos específicos de la aplicación con una superficie.</span><span class="sxs-lookup"><span data-stu-id="a36ce-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="a36ce-106">Por ejemplo, una superficie que representa un mapa en un juego podría contener información sobre el terreno.</span><span class="sxs-lookup"><span data-stu-id="a36ce-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="a36ce-107">Una superficie puede tener más de un búfer de datos privado.</span><span class="sxs-lookup"><span data-stu-id="a36ce-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="a36ce-108">Cada búfer se identifica mediante un GUID que se proporciona al adjuntar los datos a la superficie.</span><span class="sxs-lookup"><span data-stu-id="a36ce-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="a36ce-109">Para almacenar datos de la superficie privada, use SetPrivateData, pasando un puntero al búfer de origen, el tamaño de los datos y un GUID definido por la aplicación para los datos.</span><span class="sxs-lookup"><span data-stu-id="a36ce-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="a36ce-110">Opcionalmente, los datos de origen pueden existir en el formulario de un objeto COM. en este caso, se pasa un puntero al puntero de interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del objeto y se establece la \_ marca IUNKNOWNPOINTER de D3DSPD.</span><span class="sxs-lookup"><span data-stu-id="a36ce-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="a36ce-111">SetPrivateData asigna un búfer interno para los datos y lo copia.</span><span class="sxs-lookup"><span data-stu-id="a36ce-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="a36ce-112">Después, puede liberar de forma segura el búfer de origen o el objeto.</span><span class="sxs-lookup"><span data-stu-id="a36ce-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="a36ce-113">La referencia de búfer interno o de interfaz se libera cuando se llama a FreePrivateData.</span><span class="sxs-lookup"><span data-stu-id="a36ce-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="a36ce-114">Esto sucede automáticamente cuando se libera la superficie.</span><span class="sxs-lookup"><span data-stu-id="a36ce-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="a36ce-115">Para recuperar los datos privados de una superficie, debe asignar un búfer con el tamaño correcto y, a continuación, llamar al método GetPrivateData y pasar el GUID que se asignó a los datos.</span><span class="sxs-lookup"><span data-stu-id="a36ce-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="a36ce-116">Usted es responsable de liberar cualquier memoria dinámica que use para este búfer.</span><span class="sxs-lookup"><span data-stu-id="a36ce-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="a36ce-117">Si los datos son un objeto COM, este método recupera el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a36ce-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="a36ce-118">Si no sabe lo grande que puede asignar un búfer, llame primero a GetPrivateData con cero en pSizeOfData.</span><span class="sxs-lookup"><span data-stu-id="a36ce-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="a36ce-119">Si se produce un error en el método con D3DERR \_ MOREDATA, se devuelve el número de bytes necesario para el búfer.</span><span class="sxs-lookup"><span data-stu-id="a36ce-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a36ce-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a36ce-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a36ce-121">Superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="a36ce-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 
