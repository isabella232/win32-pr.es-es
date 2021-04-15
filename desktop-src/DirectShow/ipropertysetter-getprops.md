---
description: El método GetProps recupera las propiedades establecidas en este objeto, con sus valores correspondientes.
ms.assetid: 2a2ac262-f5a4-4bbe-9cd2-aa7c7d359917
title: 'IPropertySetter:: GetProps (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.GetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5f512ce672cbbaca6556ad644f21c684130eb28e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690101"
---
# <a name="ipropertysettergetprops-method"></a><span data-ttu-id="8f422-103">IPropertySetter:: GetProps (método)</span><span class="sxs-lookup"><span data-stu-id="8f422-103">IPropertySetter::GetProps method</span></span>

> [!Note]  
> <span data-ttu-id="8f422-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="8f422-104">\[Deprecated.</span></span> <span data-ttu-id="8f422-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8f422-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8f422-106">El `GetProps` método recupera las propiedades establecidas en este objeto, con sus valores correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8f422-106">The `GetProps` method retrieves the properties set on this object, with their corresponding values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f422-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8f422-107">Syntax</span></span>


```C++
HRESULT GetProps(
  [out] LONG         *pcParams,
  [out] DEXTER_PARAM **paParam,
  [out] DEXTER_VALUE **paValue
);
```



## <a name="parameters"></a><span data-ttu-id="8f422-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f422-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f422-109">*pcParams* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f422-109">*pcParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f422-110">Recibe el número de estructuras devueltas en *param*.</span><span class="sxs-lookup"><span data-stu-id="8f422-110">Receives the number of structures returned in *paParam*.</span></span>

</dd> <dt>

<span data-ttu-id="8f422-111">*param* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f422-111">*paParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f422-112">Dirección de un puntero a una matriz de estructuras de [**\_ parámetros de Dexterity**](dexter-param.md) .</span><span class="sxs-lookup"><span data-stu-id="8f422-112">Address of a pointer to an array of [**DEXTER\_PARAM**](dexter-param.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="8f422-113">*Pavalue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8f422-113">*paValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f422-114">Dirección de un puntero a una matriz de estructuras de [**\_ valor de Dexterity**](dexter-value.md) .</span><span class="sxs-lookup"><span data-stu-id="8f422-114">Address of a pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f422-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f422-115">Return value</span></span>

<span data-ttu-id="8f422-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="8f422-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8f422-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8f422-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f422-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f422-118">Remarks</span></span>

<span data-ttu-id="8f422-119">Para cada propiedad devuelta en *param*, el miembro **nvalores** indica el número de estructuras de [**\_ valor de Dexterity**](dexter-value.md) asociadas a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f422-119">For each property returned in *paParam*, the **nValues** member indicates the number of [**DEXTER\_VALUE**](dexter-value.md) structures associated with the property.</span></span> <span data-ttu-id="8f422-120">Los pares se devuelven en orden de tiempo ascendente para cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="8f422-120">The pairs are returned in ascending time order for each property.</span></span>

<span data-ttu-id="8f422-121">Cuando haya terminado de usar las estructuras devueltas, llame a [**IPropertySetter:: FreeProps**](ipropertysetter-freeprops.md) para liberar los recursos asignados por este método.</span><span class="sxs-lookup"><span data-stu-id="8f422-121">When you are finished using the returned structures, call [**IPropertySetter::FreeProps**](ipropertysetter-freeprops.md) to free the resources allocated by this method.</span></span>

> [!Note]  
> <span data-ttu-id="8f422-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="8f422-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8f422-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8f422-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8f422-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8f422-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8f422-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8f422-125">Examples</span></span>

<span data-ttu-id="8f422-126">En el ejemplo de código siguiente se muestra cómo recorrer en iteración todos los valores de una instancia del establecedor de propiedad:</span><span class="sxs-lookup"><span data-stu-id="8f422-126">The following code example shows how to iterate through all the values on an instance of the property setter:</span></span>


```C++
IPropertySetter *pSetter = NULL;
// Get a valid IPropertySetter pointer (not shown).

DEXTER_PARAM *pParam;
DEXTER_VALUE *pValue;
LONG count;

hr = pSetter->GetProps(&count, &pParam, &pValue);

LONG num = 0;
for (LONG i = 0; i < count; i++)
{
    for (LONG j = 0; j < pParam[i].nValues; j++)
    {
        // pValue[num] is the next value in the sequence for pParam[i]
    }
    num += pParam[i].nValues;
}
```



## <a name="requirements"></a><span data-ttu-id="8f422-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f422-127">Requirements</span></span>



| <span data-ttu-id="8f422-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f422-128">Requirement</span></span> | <span data-ttu-id="8f422-129">Value</span><span class="sxs-lookup"><span data-stu-id="8f422-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f422-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f422-130">Header</span></span><br/>  | <dl> <span data-ttu-id="8f422-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f422-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8f422-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8f422-132">Library</span></span><br/> | <dl> <span data-ttu-id="8f422-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f422-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f422-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f422-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f422-135">**Interfaz IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="8f422-135">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="8f422-136">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="8f422-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




