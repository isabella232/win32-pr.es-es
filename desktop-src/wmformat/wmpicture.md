---
title: WM/imagen
description: El atributo WM/imagen contiene una imagen relacionada con el contenido.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Formato de Windows Media WM/imagen
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994706"
---
# <a name="wmpicture"></a><span data-ttu-id="9c21d-104">WM/imagen</span><span class="sxs-lookup"><span data-stu-id="9c21d-104">WM/Picture</span></span>

<span data-ttu-id="9c21d-105">El atributo **WM/imagen** contiene una imagen relacionada con el contenido.</span><span class="sxs-lookup"><span data-stu-id="9c21d-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9c21d-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="9c21d-106">Global Constant</span></span>

<span data-ttu-id="9c21d-107">g \_ wszWMPicture</span><span class="sxs-lookup"><span data-stu-id="9c21d-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="9c21d-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9c21d-108">Data Type</span></span>

<span data-ttu-id="9c21d-109">[**WM \_ IMAGEN**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ tipo WMT \_ binario**)</span><span class="sxs-lookup"><span data-stu-id="9c21d-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="9c21d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c21d-110">Remarks</span></span>

<span data-ttu-id="9c21d-111">Este atributo es compatible con el marco ID3, APIC.</span><span class="sxs-lookup"><span data-stu-id="9c21d-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="9c21d-112">La especificación ID3 del marco APIC estipula que, aunque puede haber cualquier número de Marcos APIC asociados a un archivo, solo uno puede ser de tipo 1 y solo uno puede ser de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="9c21d-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="9c21d-113">La especificación también indica que la descripción de la imagen no puede tener más de 64 caracteres, pero puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="9c21d-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="9c21d-114">Los atributos de WM/imagen agregados con los objetos del SDK de Windows Media Format no se validan automáticamente para ajustarse a las especificaciones ID3.</span><span class="sxs-lookup"><span data-stu-id="9c21d-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="9c21d-115">Debe agregar código en la aplicación para realizar validaciones si desea mantener la compatibilidad completa con ID3.</span><span class="sxs-lookup"><span data-stu-id="9c21d-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c21d-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c21d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c21d-117">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="9c21d-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="9c21d-118">**imagen de WM \_**</span><span class="sxs-lookup"><span data-stu-id="9c21d-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




