---
description: En este tema se enumeran los métodos DrawString de la clase Graphics. Para obtener una lista completa de los métodos de la clase Graphics, vea Graphics.
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: Métodos Graphics. DrawString (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987535"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="ac35b-104">Graphics. DrawString (métodos)</span><span class="sxs-lookup"><span data-stu-id="ac35b-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="ac35b-105">En este tema se enumeran los métodos DrawString de la clase [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ac35b-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="ac35b-106">Para obtener una lista completa de los métodos de la clase **Graphics** , vea [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="ac35b-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="ac35b-107">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="ac35b-107">Overload list</span></span>



| <span data-ttu-id="ac35b-108">Método</span><span class="sxs-lookup"><span data-stu-id="ac35b-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="ac35b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac35b-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac35b-110">[**DrawString (WCHAR \* , int, Font \* ,& de PointF, Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="ac35b-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="ac35b-111">El método [**Graphics::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) dibuja una cadena basada en una fuente y un origen para la cadena.</span><span class="sxs-lookup"><span data-stu-id="ac35b-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="ac35b-112">[**DrawString (WCHAR \* , int, Font \* , RectF&, StringFormat \* , Brush \* )**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ac35b-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="ac35b-113">El método [**Graphics::D rawstring**](/previous-versions//ms535991(v=vs.85)) dibuja una cadena basada en una fuente, un rectángulo de diseño y un formato.</span><span class="sxs-lookup"><span data-stu-id="ac35b-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="ac35b-114">[**DrawString (WCHAR \* , int, Font \* , PointF&, StringFormat \* , Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="ac35b-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="ac35b-115">El método [**Graphics::D rawstring**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) dibuja una cadena basándose en una fuente, un origen de cadena y un formato.</span><span class="sxs-lookup"><span data-stu-id="ac35b-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="ac35b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac35b-116">Requirements</span></span>



| <span data-ttu-id="ac35b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac35b-117">Requirement</span></span> | <span data-ttu-id="ac35b-118">Value</span><span class="sxs-lookup"><span data-stu-id="ac35b-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac35b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ac35b-119">Header</span></span><br/> | <dl> <span data-ttu-id="ac35b-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac35b-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
