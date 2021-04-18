---
description: Obtiene el objeto ISearchItem si la dirección URL representa un origen de datos de Shell real (también conocido como una extensión de espacio de nombres de Shell).
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: 'ISearchItem:: GetParentFolder (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705492"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="d7820-103">ISearchItem:: GetParentFolder (método)</span><span class="sxs-lookup"><span data-stu-id="d7820-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="d7820-104">Obtiene el objeto [**ISearchItem**](-search-isearchitem.md) si la dirección URL representa un origen de datos de Shell real (también conocido como una extensión de espacio de nombres de Shell).</span><span class="sxs-lookup"><span data-stu-id="d7820-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="d7820-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7820-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="d7820-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7820-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7820-107">*IShellFolder* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7820-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7820-108">Tipo: **ppShellFolder \* \***</span><span class="sxs-lookup"><span data-stu-id="d7820-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="d7820-109">En la devolución, contiene la dirección de un puntero a la carpeta que contiene la dirección URL actual.</span><span class="sxs-lookup"><span data-stu-id="d7820-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="d7820-110">Todos los objetos de carpeta de espacio de nombres de Shell exponen la [interfaz IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) y se usan sus métodos para administrar carpetas.</span><span class="sxs-lookup"><span data-stu-id="d7820-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="d7820-111">*LPITEMIDLIST* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d7820-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7820-112">Tipo: \**ppidl \** _</span><span class="sxs-lookup"><span data-stu-id="d7820-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="d7820-113">En la devolución, contiene la dirección de un puntero a una lista de identificadores de elementos (PIDL) que identifica la carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="d7820-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="d7820-114">El parámetro _LPITEMIDLIST \* puede hacer referencia a un objeto en cualquier nivel debajo de la carpeta primaria en la jerarquía de espacios de nombres y, por tanto, puede ser un puntero de varios niveles a un **PIDL** relativo a la carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="d7820-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7820-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7820-115">Return value</span></span>

<span data-ttu-id="d7820-116">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7820-116">Type: **HRESULT**</span></span>

<span data-ttu-id="d7820-117">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="d7820-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7820-118">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d7820-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7820-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7820-119">Remarks</span></span>

<span data-ttu-id="d7820-120">El método **ISearchItem:: GetParentFolder** solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="d7820-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="d7820-121">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**ISearchItem**](-search-isearchitem.md) y las siguientes API: las interfaces [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md)y [**ISearchProtocolUI**](-search-isearchprotocolui.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="d7820-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7820-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7820-122">Requirements</span></span>



| <span data-ttu-id="d7820-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7820-123">Requirement</span></span> | <span data-ttu-id="d7820-124">Value</span><span class="sxs-lookup"><span data-stu-id="d7820-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7820-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7820-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d7820-126">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7820-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7820-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7820-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d7820-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d7820-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d7820-129">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d7820-129">Redistributable</span></span><br/>          | <span data-ttu-id="d7820-130">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d7820-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d7820-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7820-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7820-132">**ISearchItem**</span><span class="sxs-lookup"><span data-stu-id="d7820-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
