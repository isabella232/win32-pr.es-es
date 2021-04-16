---
description: Operadores de asignación de multiplicación.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: Operator * = operadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696704"
---
# <a name="operator--operators"></a><span data-ttu-id="0b4b0-103">Operator = (operador) \*</span><span class="sxs-lookup"><span data-stu-id="0b4b0-103">operator \*= operators</span></span>

<span data-ttu-id="0b4b0-104">Operadores de asignación y multiplicación</span><span class="sxs-lookup"><span data-stu-id="0b4b0-104">Multiplication assignment operators</span></span>

### <a name="overload-list"></a><span data-ttu-id="0b4b0-105">Lista de sobrecarga</span><span class="sxs-lookup"><span data-stu-id="0b4b0-105">Overload list</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="0b4b0-106">Operator</span><span class="sxs-lookup"><span data-stu-id="0b4b0-106">Operator</span></span></th>
<th style="text-align: left;"><span data-ttu-id="0b4b0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b4b0-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="0b4b0-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR:: Operator \* = (XMVECTOR&, float)</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b4b0-108"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,float)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="0b4b0-109">Multiplica una <code>XMVECTOR</code> instancia por un valor de punto flotante y devuelve una referencia a la instancia actualizada.</span><span class="sxs-lookup"><span data-stu-id="0b4b0-109">Multiplies an <code>XMVECTOR</code> instance by a floating point value and returns a reference to the updated instance.</span></span> <br/> <span data-ttu-id="0b4b0-110"><code>operator \*=</code>Multiplica cada componente de la instancia actual del <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por un valor de punto flotante especificado y devuelve una referencia a la instancia actual actualizada.</span><span class="sxs-lookup"><span data-stu-id="0b4b0-110">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by a specified floating point value, returning a reference to the updated current instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0b4b0-111">Este operador solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="0b4b0-111">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="0b4b0-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR:: Operator \* = (XMVECTOR&, XMVECTOR)</strong></a></span><span class="sxs-lookup"><span data-stu-id="0b4b0-112"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR::operator \*= (XMVECTOR&,XMVECTOR)</strong></a></span></span></td>
<td style="text-align: left;"><span data-ttu-id="0b4b0-113">Multiplica una <code>XMVECTOR</code> instancia por una segunda instancia, devolviendo una referencia a la instancia inicial actualizada.</span><span class="sxs-lookup"><span data-stu-id="0b4b0-113">Multiplies one <code>XMVECTOR</code> instance by a second instance, returning a reference to the updated initial instance.</span></span> <br/> <span data-ttu-id="0b4b0-114">El <code>operator \*=</code> multiplica cada componente de la instancia actual del <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por el componente correspondiente de una segunda instancia especificada de <code>XMVECTOR</code> , y devuelve una referencia a la instancia inicial actualizada.</span><span class="sxs-lookup"><span data-stu-id="0b4b0-114">The <code>operator \*=</code> multiplies each component of the current instance of <a href="xmvector-data-type.md"><strong>XMVECTOR Data Type</strong></a> by the corresponding component in a second specified instance of <code>XMVECTOR</code>, returning a reference to the updated initial instance.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0b4b0-115">Este operador solo está disponible en C++.</span><span class="sxs-lookup"><span data-stu-id="0b4b0-115">This operator is only available under C++.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a><span data-ttu-id="0b4b0-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b4b0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b4b0-117">Operadores XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="0b4b0-117">XMVECTOR Operators</span></span>](ovw-xmvector-operators.md)
</dt> <dt>

<span data-ttu-id="0b4b0-118">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0b4b0-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b4b0-119">**XMVECTOR, tipo de datos**</span><span class="sxs-lookup"><span data-stu-id="0b4b0-119">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 
