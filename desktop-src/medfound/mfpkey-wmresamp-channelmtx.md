---
description: Especifica la matriz de canales, que se usa para convertir los canales de origen en los canales de destino (por ejemplo, para convertir de 5,1 a estéreo).
ms.assetid: 2f2a82bd-f051-4b05-a9c8-37aa4403fab4
title: Propiedad MFPKEY_WMRESAMP_CHANNELMTX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e39f9a9344dd080362859592fcf1f71657ee8f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696891"
---
# <a name="mfpkey_wmresamp_channelmtx-property"></a><span data-ttu-id="3485a-103">\_ \_ Propiedad CHANNELMTX de MFPKEY WMRESAMP</span><span class="sxs-lookup"><span data-stu-id="3485a-103">MFPKEY\_WMRESAMP\_CHANNELMTX Property</span></span>

<span data-ttu-id="3485a-104">Especifica la matriz de canales, que se usa para convertir los canales de origen en los canales de destino (por ejemplo, para convertir de 5,1 a estéreo).</span><span class="sxs-lookup"><span data-stu-id="3485a-104">Specifies the channel matrix, which is used to convert the source channels into the destination channels (for example, to convert 5.1 to stereo).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3485a-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3485a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3485a-106">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="3485a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="3485a-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="3485a-107">Data Type</span></span>

<span data-ttu-id="3485a-108">Matriz de VT \_ I4 \| VT \_</span><span class="sxs-lookup"><span data-stu-id="3485a-108">VT\_I4 \| VT\_ARRAY</span></span>

## <a name="applies-to"></a><span data-ttu-id="3485a-109">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="3485a-109">Applies To</span></span>

-   [<span data-ttu-id="3485a-110">DSP de remuestreador de audio</span><span class="sxs-lookup"><span data-stu-id="3485a-110">Audio Resampler DSP</span></span>](audioresampler.md)

## <a name="remarks"></a><span data-ttu-id="3485a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3485a-111">Remarks</span></span>

<span data-ttu-id="3485a-112">El valor de la propiedad es una matriz de coeficientes NS x ND, donde NS es el número de canales de origen y ND es el número de canales de destino.</span><span class="sxs-lookup"><span data-stu-id="3485a-112">The value of the property is a matrix of Ns x Nd coefficients, where Ns is the number of source channels and Nd is the number of destination channels.</span></span> <span data-ttu-id="3485a-113">Los coeficientes se especifican en decibelios mediante la siguiente fórmula:</span><span class="sxs-lookup"><span data-stu-id="3485a-113">Coefficients are specified in decibels using the following formula:</span></span>

<span data-ttu-id="3485a-114">Inter (65536 \* 20 \* Log10 (dB))</span><span class="sxs-lookup"><span data-stu-id="3485a-114">(int)(65536\*20\*log10(dB))</span></span>

<span data-ttu-id="3485a-115">La matriz se almacena como una matriz en el orden principal de la fila, donde el número de fila es el canal de origen y el número de columna es el canal de destino.</span><span class="sxs-lookup"><span data-stu-id="3485a-115">The matrix is stored as an array in row-major order where the row number is the source channel and the column number is the destination channel.</span></span>

<span data-ttu-id="3485a-116">Por lo tanto, si la matriz es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="3485a-116">Thus, if the matrix is the following:</span></span>

``` syntax
00       01       ...      0(Ns-1)
10       11       ...      1(Ns-1)
...      ...      ...      ...
(Nd-1)0 (Nd-1)1 ... (Nd-1)(Ns-1)
```

<span data-ttu-id="3485a-117">a continuación, debe especificar la matriz como:</span><span class="sxs-lookup"><span data-stu-id="3485a-117">then you would specify the array as:</span></span>

``` syntax
[ 00, 01, ..., 0(Ns-1), 10, 11, ..., 1(Ns-1), ..., (Nd-1)0, (Nd-1)1, ..., (Nd-1)(Ns-1) ]
```

## <a name="requirements"></a><span data-ttu-id="3485a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3485a-118">Requirements</span></span>



| <span data-ttu-id="3485a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3485a-119">Requirement</span></span> | <span data-ttu-id="3485a-120">Value</span><span class="sxs-lookup"><span data-stu-id="3485a-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3485a-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3485a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3485a-122">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3485a-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3485a-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3485a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3485a-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3485a-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3485a-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3485a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3485a-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3485a-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3485a-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3485a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3485a-128">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3485a-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
