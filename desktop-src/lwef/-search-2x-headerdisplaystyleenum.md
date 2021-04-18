---
title: Enumeración HeaderDisplayStyle
description: Usado por IResultsViewer HeaderStyle para establecer o devolver el estilo de encabezado actual.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Enumeración HeaderDisplayStyle características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699676"
---
# <a name="headerdisplaystyle-enumeration"></a><span data-ttu-id="9f890-104">Enumeración HeaderDisplayStyle</span><span class="sxs-lookup"><span data-stu-id="9f890-104">HeaderDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="9f890-105">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9f890-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9f890-106">En versiones posteriores, use la [API de búsqueda de Windows](../search/-search-reference-entry-page.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="9f890-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9f890-107">Usado por [**IResultsViewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) para establecer o devolver el estilo de encabezado actual.</span><span class="sxs-lookup"><span data-stu-id="9f890-107">Used by [**IResultsViewer::HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) to set or return the current header style.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f890-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f890-108">Syntax</span></span>


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="9f890-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="9f890-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="9f890-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span><span class="sxs-lookup"><span data-stu-id="9f890-110"><span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**</span></span>
</dt> <dd>

<span data-ttu-id="9f890-111">Indica o establece el uso de encabezados completos.</span><span class="sxs-lookup"><span data-stu-id="9f890-111">Indicates or sets the use of full headers.</span></span>

</dd> <dt>

<span data-ttu-id="9f890-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span><span class="sxs-lookup"><span data-stu-id="9f890-112"><span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**</span></span>
</dt> <dd>

<span data-ttu-id="9f890-113">Indica o establece el uso de encabezados de compactación.</span><span class="sxs-lookup"><span data-stu-id="9f890-113">Indicates or sets the use of compact headers.</span></span>

</dd> <dt>

<span data-ttu-id="9f890-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noheader**</span><span class="sxs-lookup"><span data-stu-id="9f890-114"><span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**NoHeader**</span></span>
</dt> <dd>

<span data-ttu-id="9f890-115">Indica o establece el uso de ningún encabezado.</span><span class="sxs-lookup"><span data-stu-id="9f890-115">Indicates or sets the use of no headers.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9f890-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f890-116">Requirements</span></span>



| <span data-ttu-id="9f890-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f890-117">Requirement</span></span> | <span data-ttu-id="9f890-118">Value</span><span class="sxs-lookup"><span data-stu-id="9f890-118">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9f890-119">IDL</span><span class="sxs-lookup"><span data-stu-id="9f890-119">IDL</span></span><br/> | <dl> <span data-ttu-id="9f890-120"><dt>WdsView. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f890-120"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





