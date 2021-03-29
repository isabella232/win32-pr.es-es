---
description: Mergemod.dll llama al método ProvideTextData para recuperar datos de texto de la herramienta cliente. Mergemod.dll proporciona el nombre de la entrada correspondiente en la tabla ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Método ConfigureModule. ProvideTextData (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653921"
---
# <a name="configuremoduleprovidetextdata-method"></a><span data-ttu-id="1abe5-104">ConfigureModule. ProvideTextData, método</span><span class="sxs-lookup"><span data-stu-id="1abe5-104">ConfigureModule.ProvideTextData method</span></span>

<span data-ttu-id="1abe5-105">Mergemod.dll llama al método **ProvideTextData** para recuperar datos de texto de la herramienta cliente.</span><span class="sxs-lookup"><span data-stu-id="1abe5-105">The **ProvideTextData** method is called by Mergemod.dll to retrieve text data from the client tool.</span></span> <span data-ttu-id="1abe5-106">Mergemod.dll proporciona el *nombre* de la entrada correspondiente en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1abe5-106">Mergemod.dll provides the *Name* from the corresponding entry in the ModuleConfiguration table.</span></span>

<span data-ttu-id="1abe5-107">La herramienta debe devolver S \_ correcto y proporcionar el texto de personalización adecuado en ConfigData.</span><span class="sxs-lookup"><span data-stu-id="1abe5-107">The tool should return S\_OK and provide the appropriate customization text in ConfigData.</span></span> <span data-ttu-id="1abe5-108">La herramienta cliente es responsable de la asignación de los datos, pero Mergemod.dlles responsable de liberar la memoria.</span><span class="sxs-lookup"><span data-stu-id="1abe5-108">The client tool is responsible for allocating the data, but Mergemod.dllis responsible for releasing the memory.</span></span> <span data-ttu-id="1abe5-109">Este argumento debe ser un objeto **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="1abe5-109">This argument MUST be a **BSTR** object.</span></span> <span data-ttu-id="1abe5-110">**LPCWSTR** no se acepta.</span><span class="sxs-lookup"><span data-stu-id="1abe5-110">**LPCWSTR** is NOT accepted.</span></span>

<span data-ttu-id="1abe5-111">Si la herramienta no proporciona ningún dato de configuración para este valor de *nombre* , la función debe devolver S \_ false.</span><span class="sxs-lookup"><span data-stu-id="1abe5-111">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="1abe5-112">En este caso Mergemod.dll omite el valor del argumento ConfigData y usa el valor predeterminado de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1abe5-112">In this case Mergemod.dll ignores the value of the ConfigData argument and uses the Default value from the ModuleConfiguration table.</span></span>

<span data-ttu-id="1abe5-113">Cualquier código de retorno distinto de S \_ OK o s \_ false producirá un error que se registrará (si hay un registro abierto) y dará lugar a errores de combinación.</span><span class="sxs-lookup"><span data-stu-id="1abe5-113">Any return code other than S\_OK or S\_FALSE will cause an error to be logged (if a log is open) and will result in the merge failing.</span></span>

<span data-ttu-id="1abe5-114">Dado que esta función sigue la Convención **BSTR** estándar, NULL es equivalente a la cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1abe5-114">Because this function follows standard **BSTR** convention, null is equivalent to the empty string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1abe5-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1abe5-115">Syntax</span></span>


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="1abe5-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1abe5-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1abe5-117">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="1abe5-117">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="1abe5-118">Nombre del elemento para el que se recuperan los datos.</span><span class="sxs-lookup"><span data-stu-id="1abe5-118">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="1abe5-119">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="1abe5-119">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="1abe5-120">Puntero al texto de personalización.</span><span class="sxs-lookup"><span data-stu-id="1abe5-120">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1abe5-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1abe5-121">Return value</span></span>

<span data-ttu-id="1abe5-122">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1abe5-122">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1abe5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1abe5-123">Remarks</span></span>

<span data-ttu-id="1abe5-124">Es posible que el cliente no se llame más de una vez para cada registro de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1abe5-124">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="1abe5-125">Tenga en cuenta que Mergemod.dll nunca realiza varias llamadas al cliente para el mismo valor "Name".</span><span class="sxs-lookup"><span data-stu-id="1abe5-125">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="1abe5-126">Si no hay ningún registro en la tabla ModuleSubstitution que usa la propiedad, una entrada de la tabla ModuleConfiguration no hace ninguna llamada al cliente.</span><span class="sxs-lookup"><span data-stu-id="1abe5-126">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="1abe5-127">C++</span><span class="sxs-lookup"><span data-stu-id="1abe5-127">C++</span></span>

<span data-ttu-id="1abe5-128">Consulte [**función ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span><span class="sxs-lookup"><span data-stu-id="1abe5-128">See [**ProvideTextData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="1abe5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1abe5-129">Requirements</span></span>



| <span data-ttu-id="1abe5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1abe5-130">Requirement</span></span> | <span data-ttu-id="1abe5-131">Value</span><span class="sxs-lookup"><span data-stu-id="1abe5-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1abe5-132">Versión</span><span class="sxs-lookup"><span data-stu-id="1abe5-132">Version</span></span><br/> | <span data-ttu-id="1abe5-133">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="1abe5-133">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1abe5-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1abe5-134">Header</span></span><br/>  | <dl> <span data-ttu-id="1abe5-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1abe5-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1abe5-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1abe5-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="1abe5-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1abe5-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




