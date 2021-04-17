---
title: Verbo
description: Especifica los verbos que se van a registrar para una aplicación.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Clave del registro Verb COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105714465"
---
# <a name="verb"></a><span data-ttu-id="7525a-104">Verbo</span><span class="sxs-lookup"><span data-stu-id="7525a-104">Verb</span></span>

<span data-ttu-id="7525a-105">Especifica los verbos que se van a registrar para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7525a-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="7525a-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="7525a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="7525a-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7525a-107">Remarks</span></span>

<span data-ttu-id="7525a-108">Cada verbo es un valor de **reg \_ SZ** con el formato "*nombre*, *\_ marca de menú*, *\_ marca de verbo*".</span><span class="sxs-lookup"><span data-stu-id="7525a-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="7525a-109">Los verbos se deben numerar consecutivamente.</span><span class="sxs-lookup"><span data-stu-id="7525a-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="7525a-110">El *nombre* describe cómo se anexa el verbo mediante una llamada de función [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) .</span><span class="sxs-lookup"><span data-stu-id="7525a-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="7525a-111">Por ejemplo, "&Play".</span><span class="sxs-lookup"><span data-stu-id="7525a-111">For example, "&Play".</span></span>

<span data-ttu-id="7525a-112">El valor de la *\_ marca de menú* indica cómo debe aparecer el verbo en el menú.</span><span class="sxs-lookup"><span data-stu-id="7525a-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="7525a-113">Se admiten todas las marcas admitidas por [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) , excepto en el caso del \_ elemento emergente MF Bitmap, MF \_ OWNERDRAW y MF \_ Popup.</span><span class="sxs-lookup"><span data-stu-id="7525a-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="7525a-114">El valor de *\_ marcador de verbo* describe los atributos de los verbos.</span><span class="sxs-lookup"><span data-stu-id="7525a-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="7525a-115">Use uno de los valores de [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)o 0.</span><span class="sxs-lookup"><span data-stu-id="7525a-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="7525a-116">Para obtener más información, vea [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)y [**IOleObject:: EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span><span class="sxs-lookup"><span data-stu-id="7525a-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7525a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7525a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7525a-118">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="7525a-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="7525a-119">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="7525a-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="7525a-120">**OLEVERBATTRIB**</span><span class="sxs-lookup"><span data-stu-id="7525a-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 