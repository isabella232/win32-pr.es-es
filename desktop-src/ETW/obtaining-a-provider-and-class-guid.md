---
description: Para obtener un GUID de proveedor o GUID de clase de seguimiento de eventos, puede usar la herramienta Uuidgen.exe o Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtener un proveedor y un GUID de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985715"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="a3a25-103">Obtener un proveedor y un GUID de clase</span><span class="sxs-lookup"><span data-stu-id="a3a25-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="a3a25-104">Para obtener un GUID de proveedor o GUID de clase de seguimiento de eventos, puede usar la herramienta Uuidgen.exe o Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="a3a25-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="a3a25-105">Si usa la herramienta Uuidgen.exe, use la opción-d para crear una macro definir \_ GUID C, como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3a25-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="a3a25-106">Para obtener información sobre el uso de la herramienta Uuidgen.exe, use el</span><span class="sxs-lookup"><span data-stu-id="a3a25-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="a3a25-107">.</span><span class="sxs-lookup"><span data-stu-id="a3a25-107">option.</span></span> <span data-ttu-id="a3a25-108">Si usa la macro definir \_ GUID C para definir el GUID, debe incluir \# define INITGUID antes de las definiciones de GUID, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3a25-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

<span data-ttu-id="a3a25-109">El kit de desarrollo de software (SDK) de Microsoft Windows y Microsoft Visual Studio incluyen la herramienta Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="a3a25-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="a3a25-110">La herramienta Guidgen.exe tiene una interfaz de usuario que le permite seleccionar varios formatos.</span><span class="sxs-lookup"><span data-stu-id="a3a25-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="a3a25-111">Debe usar el formato que crea un GUID de constante estática, tal como se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3a25-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



