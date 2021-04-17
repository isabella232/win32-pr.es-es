---
description: Especifica si el codificador debe comprobar la coherencia de los datos entre las pasadas al realizar la codificación VBR de dos pasos. Lectura y escritura.
ms.assetid: 68750820-e931-41c2-9d12-89ab83b4b97e
title: Propiedad MFPKEY_CHECKDATACONSISTENCY2P (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc706712ef1e8bff36a118031fde155bb9bda31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698626"
---
# <a name="mfpkey_checkdataconsistency2p-property"></a><span data-ttu-id="98739-104">\_Propiedad CHECKDATACONSISTENCY2P de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="98739-104">MFPKEY\_CHECKDATACONSISTENCY2P Property</span></span>

<span data-ttu-id="98739-105">Especifica si el codificador debe comprobar la coherencia de los datos entre las pasadas al realizar la codificación VBR de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="98739-105">Specifies whether whether the encoder should check for data consistency across passes when performing two-pass VBR encoding.</span></span> <span data-ttu-id="98739-106">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="98739-106">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="98739-107">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="98739-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="98739-108">Solo está disponible mediante [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="98739-108">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="98739-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="98739-109">Data Type</span></span>

<span data-ttu-id="98739-110">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="98739-110">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="98739-111">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="98739-111">Default Value</span></span>

<span data-ttu-id="98739-112">**VARIANTE \_ true**</span><span class="sxs-lookup"><span data-stu-id="98739-112">**VARIANT\_TRUE**</span></span>

## <a name="remarks"></a><span data-ttu-id="98739-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98739-113">Remarks</span></span>

<span data-ttu-id="98739-114">Si deja esta propiedad en su valor predeterminado de **Variant \_ true**, el codificador comprueba que los ejemplos de entrada coinciden entre los dos pasos y produce un error si detecta una discrepancia.</span><span class="sxs-lookup"><span data-stu-id="98739-114">If you leave this property at its default value of **VARIANT\_TRUE**, the encoder verifies that the input samples match between the two passes, and fails if it detects a discrepancy.</span></span> <span data-ttu-id="98739-115">El escenario principal que conduce a una discrepancia es cuando la entrada procede de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98739-115">The main scenario that leads to a discrepancy is when the input comes from a device.</span></span>

## <a name="requirements"></a><span data-ttu-id="98739-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98739-116">Requirements</span></span>



| <span data-ttu-id="98739-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98739-117">Requirement</span></span> | <span data-ttu-id="98739-118">Value</span><span class="sxs-lookup"><span data-stu-id="98739-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98739-119">Remoto</span><span class="sxs-lookup"><span data-stu-id="98739-119">Client</span></span><br/> | <span data-ttu-id="98739-120">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="98739-120">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="98739-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98739-121">Header</span></span><br/> | <dl> <span data-ttu-id="98739-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="98739-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98739-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="98739-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98739-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="98739-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
