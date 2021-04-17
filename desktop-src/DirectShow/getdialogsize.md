---
description: La función GetDialogSize recupera el tamaño de un cuadro de diálogo de recursos.
ms.assetid: b6c42f96-0381-493a-9503-f3bd4c6a8e1e
title: Función GetDialogSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDialogSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 34eff1882306c85446f7cc7708efea3b17fcf7e3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653839"
---
# <a name="getdialogsize-function"></a><span data-ttu-id="1423b-103">GetDialogSize función)</span><span class="sxs-lookup"><span data-stu-id="1423b-103">GetDialogSize function</span></span>

<span data-ttu-id="1423b-104">La función **GetDialogSize** recupera el tamaño de un cuadro de diálogo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1423b-104">The **GetDialogSize** function retrieves the size of a resource dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="1423b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1423b-105">Syntax</span></span>


```C++
BOOL WINAPI GetDialogSize(
   int     iResourceID,
   DLGPROC pDlgProc,
   LPARAM  lParam,
   SIZE    *pResult
);
```



## <a name="parameters"></a><span data-ttu-id="1423b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1423b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1423b-107">*iResourceID*</span><span class="sxs-lookup"><span data-stu-id="1423b-107">*iResourceID*</span></span> 
</dt> <dd>

<span data-ttu-id="1423b-108">Identificador de recursos del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1423b-108">Dialog box resource identifier.</span></span>

</dd> <dt>

<span data-ttu-id="1423b-109">*pDlgProc*</span><span class="sxs-lookup"><span data-stu-id="1423b-109">*pDlgProc*</span></span> 
</dt> <dd>

<span data-ttu-id="1423b-110">Puntero al procedimiento del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1423b-110">Pointer to the dialog box procedure.</span></span>

</dd> <dt>

<span data-ttu-id="1423b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1423b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1423b-112">Valor pasado en el mensaje de INITDIALOG de WM \_ enviado al cuadro de diálogo temporal justo después de su creación.</span><span class="sxs-lookup"><span data-stu-id="1423b-112">Value passed in the WM\_INITDIALOG message sent to the temporary dialog box just after it is created.</span></span>

</dd> <dt>

<span data-ttu-id="1423b-113">*pResult*</span><span class="sxs-lookup"><span data-stu-id="1423b-113">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="1423b-114">Puntero a una estructura de **tamaño** que recibe las dimensiones del cuadro de diálogo, en píxeles de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1423b-114">Pointer to a **SIZE** structure that receives the dimensions of the dialog box, in screen pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1423b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1423b-115">Return value</span></span>

<span data-ttu-id="1423b-116">Devuelve **true** si se encontró el recurso de cuadro de diálogo o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1423b-116">Returns **TRUE** if the dialog box resource was found, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1423b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1423b-117">Remarks</span></span>

<span data-ttu-id="1423b-118">Las páginas de propiedades pueden usar esta función para devolver el tamaño de presentación real que requieran.</span><span class="sxs-lookup"><span data-stu-id="1423b-118">Property pages can use this function to return the actual display size they require.</span></span> <span data-ttu-id="1423b-119">La mayoría de las páginas de propiedades son cuadros de diálogo y, como tales, tienen plantillas de cuadro de diálogo almacenadas en archivos de recursos.</span><span class="sxs-lookup"><span data-stu-id="1423b-119">Most property pages are dialog boxes and, as such, have dialog box templates stored in resource files.</span></span> <span data-ttu-id="1423b-120">Las plantillas utilizan unidades del cuadro de diálogo que no se asignan directamente a los píxeles de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="1423b-120">Templates use dialog box units that do not map directly onto screen pixels.</span></span> <span data-ttu-id="1423b-121">Sin embargo, la función [**GetPageInfo**](cbasepropertypage-getpageinfo.md) de una página de propiedades debe devolver el tamaño de presentación real en píxeles.</span><span class="sxs-lookup"><span data-stu-id="1423b-121">However, a property page's [**GetPageInfo**](cbasepropertypage-getpageinfo.md) function must return the actual display size in pixels.</span></span> <span data-ttu-id="1423b-122">La página de propiedades puede llamar `GetDialogSize` a para calcular el tamaño de presentación.</span><span class="sxs-lookup"><span data-stu-id="1423b-122">The property page can call `GetDialogSize` to calculate the display size.</span></span>

<span data-ttu-id="1423b-123">Esta función crea una instancia temporal del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="1423b-123">This function creates a temporary instance of the dialog box.</span></span> <span data-ttu-id="1423b-124">Para evitar que aparezca el cuadro de diálogo en la pantalla, la plantilla de cuadro de diálogo del archivo de recursos no debe tener una propiedad de WS \_ visible.</span><span class="sxs-lookup"><span data-stu-id="1423b-124">To avoid having the dialog box appear on the screen, the dialog box template in the resource file should not have a WS\_VISIBLE property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1423b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1423b-125">Requirements</span></span>



| <span data-ttu-id="1423b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1423b-126">Requirement</span></span> | <span data-ttu-id="1423b-127">Value</span><span class="sxs-lookup"><span data-stu-id="1423b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1423b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1423b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1423b-129"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1423b-129"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1423b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1423b-130">Library</span></span><br/> | <dl> <span data-ttu-id="1423b-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1423b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1423b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="1423b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1423b-133">Funciones auxiliares de páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="1423b-133">Property Page Helper Functions</span></span>](property-page-helper-functions.md)
</dt> </dl>

 

 




