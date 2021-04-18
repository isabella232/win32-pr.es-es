---
title: Complementos de origen
description: Complementos de origen
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- SDK de Windows Media Format, Complementos de origen
- Advanced Systems Format (ASF), Complementos de origen
- ASF (formato de sistemas avanzados), Complementos de origen
- Complementos de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "105720127"
---
# <a name="source-plug-ins"></a><span data-ttu-id="cf956-107">Complementos de origen</span><span class="sxs-lookup"><span data-stu-id="cf956-107">Source Plug-ins</span></span>

<span data-ttu-id="cf956-108">Un complemento de origen es una opción disponible para los desarrolladores que desean implementar su propio sistema de almacenamiento para archivos de® de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="cf956-108">A source plug-in is an option available to developers who wish to implement their own storage system for Windows Media® files.</span></span> <span data-ttu-id="cf956-109">Un complemento de origen permite esto a través de la implementación de una interfaz COM denominada **IStream**, que es una interfaz estándar para proporcionar datos.</span><span class="sxs-lookup"><span data-stu-id="cf956-109">A source plug-in enables this through the implementation of a COM interface called **IStream**, which is a standard interface for providing data.</span></span>

<span data-ttu-id="cf956-110">El complemento de origen debe escribirse como un archivo dll y su presencia se hace conocida en el SDK a través de una entrada del registro.</span><span class="sxs-lookup"><span data-stu-id="cf956-110">The source plug-in should be written as a dll, and its presence is made known to the SDK through a registry entry.</span></span> <span data-ttu-id="cf956-111">Puede haber cualquier número de complementos de origen implementados de esta manera.</span><span class="sxs-lookup"><span data-stu-id="cf956-111">There can be any number of source plug-ins implemented this way.</span></span> <span data-ttu-id="cf956-112">El complemento de origen debe exportar la función [**WMCreateStreamForURL**](wmcreatestreamforurl.md) .</span><span class="sxs-lookup"><span data-stu-id="cf956-112">The source plug-in must export the [**WMCreateStreamForURL**](wmcreatestreamforurl.md) function.</span></span>

<span data-ttu-id="cf956-113">Para registrar un complemento de origen, se debe agregar la siguiente entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="cf956-113">To register a source plug-in, the following registry entry should be added:</span></span>

<span data-ttu-id="cf956-114">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows Media \\ WMSDK \\ sources</span><span class="sxs-lookup"><span data-stu-id="cf956-114">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Media\\WMSDK\\sources</span></span>

<span data-ttu-id="cf956-115">Name = "cualquier nombre único"</span><span class="sxs-lookup"><span data-stu-id="cf956-115">Name = "any unique name"</span></span>

<span data-ttu-id="cf956-116">Valor = nombreruta del archivo dll de complemento de origen</span><span class="sxs-lookup"><span data-stu-id="cf956-116">Value = pathname of the source plug-in dll</span></span>

<span data-ttu-id="cf956-117">Una vez registrado el archivo dll, la aplicación puede usar el método **IWMReader:: Open** (con la dirección URL adecuada como parámetro) para tener acceso a los datos de la secuencia, que se pueden almacenar en archivos o en contenedores de datos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cf956-117">Once the dll has been registered, the application can use the **IWMReader::Open** method (with the appropriate URL as a parameter) to access stream data, which can be stored in files or user-defined data containers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf956-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf956-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf956-119">**IWMReader:: Open**</span><span class="sxs-lookup"><span data-stu-id="cf956-119">**IWMReader::Open**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[<span data-ttu-id="cf956-120">**Referencia de programación**</span><span class="sxs-lookup"><span data-stu-id="cf956-120">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="cf956-121">**WMCreateStreamForURL**</span><span class="sxs-lookup"><span data-stu-id="cf956-121">**WMCreateStreamForURL**</span></span>](wmcreatestreamforurl.md)
</dt> </dl>

 

 




