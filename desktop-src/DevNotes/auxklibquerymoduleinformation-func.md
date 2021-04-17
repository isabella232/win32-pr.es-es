---
description: Recupera información sobre el conjunto de módulos cargados actualmente para el sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Función AuxKlibQueryModuleInformation (AUX \_ klib. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660266"
---
# <a name="auxklibquerymoduleinformation-function"></a><span data-ttu-id="f89a7-103">AuxKlibQueryModuleInformation función)</span><span class="sxs-lookup"><span data-stu-id="f89a7-103">AuxKlibQueryModuleInformation function</span></span>

<span data-ttu-id="f89a7-104">Recupera información sobre el conjunto de módulos cargados actualmente para el sistema.</span><span class="sxs-lookup"><span data-stu-id="f89a7-104">Retrieves information about the currently loaded set of modules for the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f89a7-105">Syntax</span></span>


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a><span data-ttu-id="f89a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f89a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f89a7-107">*BufferSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f89a7-107">*BufferSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f89a7-108">En la entrada, el tamaño del búfer *QueryInfo* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="f89a7-108">On input, the size of the *QueryInfo* buffer, in bytes.</span></span> <span data-ttu-id="f89a7-109">En la salida, recibe el tamaño necesario real.</span><span class="sxs-lookup"><span data-stu-id="f89a7-109">On output, receives the actual required size.</span></span> <span data-ttu-id="f89a7-110">Dado que la lista de módulos del sistema puede cambiar entre llamadas, este valor también puede cambiar entre llamadas.</span><span class="sxs-lookup"><span data-stu-id="f89a7-110">Because the system module list can change between calls, this value can also change between calls.</span></span>

</dd> <dt>

<span data-ttu-id="f89a7-111">*Elementos de elemento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f89a7-111">*ElementSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f89a7-112">Tamaño, en bytes, de un elemento de la matriz.</span><span class="sxs-lookup"><span data-stu-id="f89a7-112">The size, in bytes, of an array element.</span></span> <span data-ttu-id="f89a7-113">Este tamaño determina el formato de la salida.</span><span class="sxs-lookup"><span data-stu-id="f89a7-113">This size determines the format of the output.</span></span>

</dd> <dt>

<span data-ttu-id="f89a7-114">*QueryInfo* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f89a7-114">*QueryInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f89a7-115">Un puntero a un búfer que recibe la información del módulo.</span><span class="sxs-lookup"><span data-stu-id="f89a7-115">A pointer to a buffer that receives the module information.</span></span> <span data-ttu-id="f89a7-116">Esta información se devuelve en una matriz cuyos elementos son una de las siguientes estructuras: [**\_ \_ \_ información básica del módulo AUX**](aux-module-basic-info-struct.md) o [**\_ \_ \_ información ampliada del módulo AUX**](aux-module-extended-info-struct.md).</span><span class="sxs-lookup"><span data-stu-id="f89a7-116">This information is returned in an array whose elements are one of the following structures: [**AUX\_MODULE\_BASIC\_INFO**](aux-module-basic-info-struct.md) or [**AUX\_MODULE\_EXTENDED\_INFO**](aux-module-extended-info-struct.md).</span></span> <span data-ttu-id="f89a7-117">La estructura específica que se utiliza depende del tamaño del elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="f89a7-117">The specific structure used depends on the specified element size.</span></span>

<span data-ttu-id="f89a7-118">Si este parámetro es **null**, la función devuelve el tamaño de búfer necesario.</span><span class="sxs-lookup"><span data-stu-id="f89a7-118">If this parameter is **NULL**, the function returns the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f89a7-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f89a7-119">Return value</span></span>

<span data-ttu-id="f89a7-120">Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.</span><span class="sxs-lookup"><span data-stu-id="f89a7-120">If the function succeeds, the return value is STATUS\_SUCCESS.</span></span>

<span data-ttu-id="f89a7-121">Si se produce un error en la función, el valor devuelto puede ser uno de los códigos de estado definidos en NTSTATUS. h, que está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="f89a7-121">If the function fails, the return value can be one of the status codes defined in Ntstatus.h, which is available in the WDK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f89a7-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f89a7-122">Remarks</span></span>

<span data-ttu-id="f89a7-123">Debe llamar a la función [**AuxKlibInitialize**](auxklibinitialize-func.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="f89a7-123">You must call the [**AuxKlibInitialize**](auxklibinitialize-func.md) function before calling this function.</span></span>

<span data-ttu-id="f89a7-124">La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).</span><span class="sxs-lookup"><span data-stu-id="f89a7-124">The object library that implements this API can be downloaded from [here](https://www.microsoft.com/?ref=go).</span></span>

## <a name="requirements"></a><span data-ttu-id="f89a7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f89a7-125">Requirements</span></span>



| <span data-ttu-id="f89a7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f89a7-126">Requirement</span></span> | <span data-ttu-id="f89a7-127">Value</span><span class="sxs-lookup"><span data-stu-id="f89a7-127">Value</span></span> |
|----------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f89a7-128">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="f89a7-128">Redistributable</span></span><br/> | <span data-ttu-id="f89a7-129">Biblioteca de API auxiliar de Windows versión 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f89a7-129">Windows Auxiliary API library version 1.0 or later</span></span><br/>                            |
| <span data-ttu-id="f89a7-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f89a7-130">Header</span></span><br/>          | <dl> <span data-ttu-id="f89a7-131"><dt>AUX \_ klib. h</dt></span><span class="sxs-lookup"><span data-stu-id="f89a7-131"><dt>Aux\_klib.h</dt></span></span> </dl>   |
| <span data-ttu-id="f89a7-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f89a7-132">Library</span></span><br/>         | <dl> <span data-ttu-id="f89a7-133"><dt>AUX \_ klib. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f89a7-133"><dt>Aux\_klib.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89a7-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="f89a7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89a7-135">**AuxKlibInitialize**</span><span class="sxs-lookup"><span data-stu-id="f89a7-135">**AuxKlibInitialize**</span></span>](auxklibinitialize-func.md)
</dt> <dt>

[<span data-ttu-id="f89a7-136">**\_ \_ información básica del módulo AUX \_**</span><span class="sxs-lookup"><span data-stu-id="f89a7-136">**AUX\_MODULE\_BASIC\_INFO**</span></span>](aux-module-basic-info-struct.md)
</dt> <dt>

[<span data-ttu-id="f89a7-137">**\_ \_ información adicional del módulo AUX \_**</span><span class="sxs-lookup"><span data-stu-id="f89a7-137">**AUX\_MODULE\_EXTENDED\_INFO**</span></span>](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




