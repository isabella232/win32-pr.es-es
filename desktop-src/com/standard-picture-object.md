---
title: Objeto de imagen estándar
description: Objeto de imagen estándar
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995658"
---
# <a name="standard-picture-object"></a><span data-ttu-id="9b623-103">Objeto de imagen estándar</span><span class="sxs-lookup"><span data-stu-id="9b623-103">Standard Picture Object</span></span>

<span data-ttu-id="9b623-104">El objeto de imagen estándar proporciona una abstracción independiente del idioma para las imágenes GDI: mapas de bits, iconos, metaarchivos y metaarchivos mejorados.</span><span class="sxs-lookup"><span data-stu-id="9b623-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="9b623-105">Al igual que con el objeto de fuente estándar, el sistema proporciona una implementación estándar de este objeto.</span><span class="sxs-lookup"><span data-stu-id="9b623-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="9b623-106">Sus interfaces principales son [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) y [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), lo que se deriva de **IDispatch** para proporcionar acceso a las propiedades de la imagen a través de la automatización OLE.</span><span class="sxs-lookup"><span data-stu-id="9b623-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="9b623-107">Se crea un objeto de imagen nuevo con [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="9b623-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="9b623-108">El objeto Picture también admite la interfaz de salida [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) para que un cliente pueda determinar cuándo cambian las propiedades de la imagen.</span><span class="sxs-lookup"><span data-stu-id="9b623-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="9b623-109">En consecuencia, el objeto Picture también admite [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) y un punto de conexión para **IPropertyNotifySink**.</span><span class="sxs-lookup"><span data-stu-id="9b623-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="9b623-110">El objeto Picture también admite [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) para que pueda guardarse y cargarse a sí mismo desde una instancia de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="9b623-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="9b623-111">Un objeto que usa un objeto de imagen internamente normalmente guardaría y cargaría la imagen como parte del propio control de persistencia del objeto.</span><span class="sxs-lookup"><span data-stu-id="9b623-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="9b623-112">La función [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifica la creación de un objeto de imagen basado en el contenido de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="9b623-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b623-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9b623-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b623-114">Propiedades del control</span><span class="sxs-lookup"><span data-stu-id="9b623-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 