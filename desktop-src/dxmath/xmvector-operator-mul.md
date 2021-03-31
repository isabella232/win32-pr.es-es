---
description: Operadores de multiplicación.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: operadores Operator *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155428"
---
# <a name="operator--operators"></a><span data-ttu-id="fbb15-103">operadores de operador \*</span><span class="sxs-lookup"><span data-stu-id="fbb15-103">operator \* operators</span></span>

<span data-ttu-id="fbb15-104">Operadores de multiplicación</span><span class="sxs-lookup"><span data-stu-id="fbb15-104">Multiplication operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="fbb15-105">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="fbb15-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="fbb15-106">Operator</span><span class="sxs-lookup"><span data-stu-id="fbb15-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="fbb15-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbb15-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="fbb15-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR:: Operator \* (float, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb15-108"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR::operator \* (float,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="fbb15-109">Multiplica un valor de punto flotante por una instancia de <code>XMVECTOR</code> , devolviendo el resultado a una nueva instancia de <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="fbb15-109">Multiply a floating point value by an instance of <code>XMVECTOR</code>, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="fbb15-110">El <code>operator \*</code> multiplica un valor de punto flotante en cada componente de una instancia de <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a>, y devuelve una nueva <code>XMVECTOR</code> instancia cuyos componentes contienen el resultado.</span><span class="sxs-lookup"><span data-stu-id="fbb15-110">The <code>operator \*</code> multiplies a floating point value against each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a>, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbb15-111">Este operador solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="fbb15-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="fbb15-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR:: Operator \* (XMVECTOR, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb15-112"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="fbb15-113">Multiplica una instancia de <code>XMVECTOR</code> por un valor de punto flotante y devuelve el resultado a una nueva instancia de <code>XMVECTOR</code> .</span><span class="sxs-lookup"><span data-stu-id="fbb15-113">Multiply an instance of <code>XMVECTOR</code> by a floating point value, returning the result a new instance of <code>XMVECTOR</code>.</span></span><br/> <span data-ttu-id="fbb15-114"><code>operator \*</code>Multiplica cada componente de una instancia de <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por un valor de punto flotante, y devuelve una nueva <code>XMVECTOR</code> instancia cuyos componentes contienen el resultado.</span><span class="sxs-lookup"><span data-stu-id="fbb15-114">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a floating point value, returning a new <code>XMVECTOR</code> instance whose components contain the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbb15-115">Este operador solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="fbb15-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="fbb15-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR:: Operator \* (XMVECTOR, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbb15-116"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR::operator \* (XMVECTOR,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="fbb15-117">Multiplica una instancia de <code>XMVECTOR</code> por una segunda instancia, devolviendo el resultado en una tercera instancia.</span><span class="sxs-lookup"><span data-stu-id="fbb15-117">Multiplies one instance of <code>XMVECTOR</code> by a second instance, returning the result in a third instance.</span></span> <br/> <span data-ttu-id="fbb15-118">El <code>operator \*</code> multiplica cada componente de una instancia de <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por el componente correspondiente en una segunda instancia de <code>XMVECTOR</code> , y devuelve una nueva <code>XMVECTOR</code> instancia de que contiene el resultado.</span><span class="sxs-lookup"><span data-stu-id="fbb15-118">The <code>operator \*</code> multiplies each component of an instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second instance of <code>XMVECTOR</code>, returning a new <code>XMVECTOR</code> instance containing the result.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="fbb15-119">Este operador solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="fbb15-119">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="fbb15-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbb15-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbb15-121">Operadores XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="fbb15-121">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="fbb15-122">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="fbb15-122">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fbb15-123">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="fbb15-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
