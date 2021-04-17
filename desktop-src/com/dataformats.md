---
title: DataFormats
description: Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.
ms.assetid: 0c9387f9-d7e0-40e7-8d86-96a79a844161
keywords:
- Clave del registro de dataFormat COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf130461a8db67cfe7fc7c56b0115b27eef6dc6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704791"
---
# <a name="dataformats"></a><span data-ttu-id="67820-104">DataFormats</span><span class="sxs-lookup"><span data-stu-id="67820-104">DataFormats</span></span>

<span data-ttu-id="67820-105">Especifica los formatos de datos predeterminados y principales admitidos por una aplicación.</span><span class="sxs-lookup"><span data-stu-id="67820-105">Specifies the default and main data formats supported by an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="67820-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="67820-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DataFormats
         DefaultFile = file/format
         GetSet
            n = formats
```

## <a name="remarks"></a><span data-ttu-id="67820-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67820-107">Remarks</span></span>

<span data-ttu-id="67820-108">El valor de *archivo o formato* especifica el formato de archivo o objeto principal predeterminado para los objetos de esta clase.</span><span class="sxs-lookup"><span data-stu-id="67820-108">The *file/format* value specifies the default main file or object format for objects of this class.</span></span>

<span data-ttu-id="67820-109">El valor *Formats* especifica una lista de formatos para las implementaciones predeterminadas de [**del EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), donde *n* es un índice entero de base cero.</span><span class="sxs-lookup"><span data-stu-id="67820-109">The *formats* value specifies a list of formats for default implementations of [**EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc), where *n* is a zero-based integer index.</span></span> <span data-ttu-id="67820-110">Por ejemplo, *n*  =  *formato*, *aspecto*, *medio*, *marca*, donde *formato* es un formato de Portapapeles, el *aspecto* es uno o varios miembros de [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *Medium* es uno o más miembros de [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed)y *Flag* es uno o más miembros de [**datadir**](/windows/win32/api/objidl/ne-objidl-datadir).</span><span class="sxs-lookup"><span data-stu-id="67820-110">For example, *n* = *format*, *aspect*, *medium*, *flag*, where *format* is a clipboard format, *aspect* is one or more members of [**DVASPECT**](/windows/win32/api/wtypes/ne-wtypes-dvaspect), *medium* is one or more members of [**TYMED**](/windows/win32/api/objidl/ne-objidl-tymed), and *flag* is one or more members of [**DATADIR**](/windows/win32/api/objidl/ne-objidl-datadir).</span></span>

## <a name="related-topics"></a><span data-ttu-id="67820-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67820-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67820-112">**IDataObject:: del EnumFormatEtc**</span><span class="sxs-lookup"><span data-stu-id="67820-112">**IDataObject::EnumFormatEtc**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)
</dt> <dt>

[<span data-ttu-id="67820-113">**IDataObject:: GetData**</span><span class="sxs-lookup"><span data-stu-id="67820-113">**IDataObject::GetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)
</dt> <dt>

[<span data-ttu-id="67820-114">**IDataObject:: SetData**</span><span class="sxs-lookup"><span data-stu-id="67820-114">**IDataObject::SetData**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata)
</dt> </dl>

 

 




