---
description: Define una memoria caché de métricas de fuente de Uniscribe.
ms.assetid: 56a98529-6ae9-4b71-bd7d-cf056a1e3683
title: SCRIPT_CACHE (Usp10. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece29fe0ed610b4576263c36c50311ef57317579
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653001"
---
# <a name="script_cache"></a><span data-ttu-id="8a567-103">caché de SCRIPT \_</span><span class="sxs-lookup"><span data-stu-id="8a567-103">SCRIPT\_CACHE</span></span>

<span data-ttu-id="8a567-104">Define una memoria caché de métricas de fuente de Uniscribe.</span><span class="sxs-lookup"><span data-stu-id="8a567-104">Defines a Uniscribe font metric cache.</span></span>


```C++
typedef void* SCRIPT_CACHE;
```



## <a name="remarks"></a><span data-ttu-id="8a567-105">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a567-105">Remarks</span></span>

<span data-ttu-id="8a567-106">Se trata de una estructura opaca.</span><span class="sxs-lookup"><span data-stu-id="8a567-106">This is an opaque structure.</span></span> <span data-ttu-id="8a567-107">La aplicación debe asignar y conservar una \_ variable de caché de script para cada estilo de carácter utilizado.</span><span class="sxs-lookup"><span data-stu-id="8a567-107">The application must allocate and retain one SCRIPT\_CACHE variable for each character style used.</span></span> <span data-ttu-id="8a567-108">La variable se debe inicializar en **null**.</span><span class="sxs-lookup"><span data-stu-id="8a567-108">The variable must be initialized to **NULL**.</span></span>

<span data-ttu-id="8a567-109">Muchas funciones de script toman una combinación de un identificador de contexto de dispositivo de hardware y una variable de caché de SCRIPTs \_ .</span><span class="sxs-lookup"><span data-stu-id="8a567-109">Many script functions take a combination of a hardware device context handle and a SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="8a567-110">En primer lugar, se intenta tener acceso a los datos de fuente mediante la variable de caché de SCRIPT \_ .</span><span class="sxs-lookup"><span data-stu-id="8a567-110">Uniscribe first attempts to access font data by using the SCRIPT\_CACHE variable.</span></span> <span data-ttu-id="8a567-111">Solo inspecciona el contexto de dispositivo de hardware Si los datos necesarios aún no están almacenados en caché.</span><span class="sxs-lookup"><span data-stu-id="8a567-111">It only inspects the hardware device context if the required data is not already cached.</span></span>

<span data-ttu-id="8a567-112">El identificador de contexto de dispositivo de hardware se puede pasar a como **null**.</span><span class="sxs-lookup"><span data-stu-id="8a567-112">The hardware device context handle can be passed to Uniscribe as **NULL**.</span></span> <span data-ttu-id="8a567-113">Si los datos requeridos por Uniscribe ya están almacenados en caché, no se tiene acceso al contexto del dispositivo y la operación continúa con normalidad.</span><span class="sxs-lookup"><span data-stu-id="8a567-113">If data required by Uniscribe is already cached, the device context is not accessed, and the operation continues normally.</span></span>

<span data-ttu-id="8a567-114">Si el contexto del dispositivo se pasa como **null** y Uniscribe tiene que tener acceso a él por cualquier motivo, Uniscribe devuelve el código de error E \_ pendiente.</span><span class="sxs-lookup"><span data-stu-id="8a567-114">If the device context is passed as **NULL** and Uniscribe needs to access it for any reason, Uniscribe returns the error code E\_PENDING.</span></span> <span data-ttu-id="8a567-115">Este código se devuelve rápidamente, lo que permite que la aplicación evite las llamadas [**SeleccionarObjeto**](/windows/win32/api/wingdi/nf-wingdi-selectobject) que consumen mucho tiempo.</span><span class="sxs-lookup"><span data-stu-id="8a567-115">This code is returned quickly, allowing the application to avoid time-consuming [**SelectObject**](/windows/win32/api/wingdi/nf-wingdi-selectobject) calls.</span></span>

## <a name="examples"></a><span data-ttu-id="8a567-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8a567-116">Examples</span></span>

<span data-ttu-id="8a567-117">El ejemplo siguiente se aplica a todas las funciones que toman una variable de caché de SCRIPTs \_ y un identificador opcional para un contexto de dispositivo de hardware.</span><span class="sxs-lookup"><span data-stu-id="8a567-117">The following example applies to all functions that take a SCRIPT\_CACHE variable and an optional handle to a hardware device context.</span></span>


```C++
hr = ScriptShape(NULL, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
if (hr == E_PENDING)
{
    // ... select font into hdc ...
    hr = ScriptShape(hdc, &sc,
                 pwcChars, cChars, cMaxGlyphs, psa, pwOutGlyphs, pwLogClust, psva, pcGlyphs);
}
```



## <a name="requirements"></a><span data-ttu-id="8a567-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a567-118">Requirements</span></span>



| <span data-ttu-id="8a567-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a567-119">Requirement</span></span> | <span data-ttu-id="8a567-120">Value</span><span class="sxs-lookup"><span data-stu-id="8a567-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8a567-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a567-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a567-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8a567-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="8a567-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a567-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a567-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8a567-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8a567-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a567-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a567-126"><dt>Usp10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a567-126"><dt>Usp10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a567-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a567-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a567-128">Uniscribe</span><span class="sxs-lookup"><span data-stu-id="8a567-128">Uniscribe</span></span>](uniscribe.md)
</dt> <dt>

[<span data-ttu-id="8a567-129">Estructuras de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="8a567-129">Uniscribe Structures</span></span>](uniscribe-structures.md)
</dt> <dt>

[<span data-ttu-id="8a567-130">Almacenamiento en caché</span><span class="sxs-lookup"><span data-stu-id="8a567-130">Caching</span></span>](caching.md)
</dt> </dl>

 

 
