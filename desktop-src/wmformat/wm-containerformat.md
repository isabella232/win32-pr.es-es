---
title: WM/ContainerFormat
description: El atributo WM/ContainerFormat especifica el tipo de archivo que se carga en el objeto que realiza la llamada.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Formato de Windows Media WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784127"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="d41cc-104">WM/ContainerFormat</span><span class="sxs-lookup"><span data-stu-id="d41cc-104">WM/ContainerFormat</span></span>

<span data-ttu-id="d41cc-105">El atributo **WM/ContainerFormat** especifica el tipo de archivo que se carga en el objeto que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="d41cc-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="d41cc-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="d41cc-106">Global Constant</span></span>

<span data-ttu-id="d41cc-107">g \_ wszWMContainerFormat</span><span class="sxs-lookup"><span data-stu-id="d41cc-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="d41cc-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="d41cc-108">Data Type</span></span>

<span data-ttu-id="d41cc-109">[**WMT \_ \_formato de almacenamiento**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**\_ tipo WMT \_ binario**)</span><span class="sxs-lookup"><span data-stu-id="d41cc-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="d41cc-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d41cc-110">Remarks</span></span>

<span data-ttu-id="d41cc-111">Este atributo se usa en lugar de **IWMProfile3:: GetStorageFormat** y **IWMProfile3:: SetStorageFormat**, que ya no se admiten.</span><span class="sxs-lookup"><span data-stu-id="d41cc-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="d41cc-112">Se trata de un atributo codificado.</span><span class="sxs-lookup"><span data-stu-id="d41cc-112">This is a coded attribute.</span></span>

<span data-ttu-id="d41cc-113">Este atributo no se puede duplicar en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="d41cc-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="d41cc-114">Si este atributo se usa para una secuencia individual, se tratará como metadatos personalizados y no enviará su significado normal a los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d41cc-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="d41cc-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="d41cc-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41cc-116">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="d41cc-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




