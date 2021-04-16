---
description: Mergemod.dll llama al método ProvideIntegerData del objeto ConfigureModule para recuperar datos enteros de la herramienta cliente.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Método ConfigureModule. ProvideIntegerData (Mergemod. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671609"
---
# <a name="configuremoduleprovideintegerdata-method"></a><span data-ttu-id="0448b-103">ConfigureModule. ProvideIntegerData, método</span><span class="sxs-lookup"><span data-stu-id="0448b-103">ConfigureModule.ProvideIntegerData method</span></span>

<span data-ttu-id="0448b-104">Mergemod.dll llama al método **ProvideIntegerData** del [**objeto ConfigureModule**](configuremodule-object.md) para recuperar datos enteros de la herramienta cliente.</span><span class="sxs-lookup"><span data-stu-id="0448b-104">The **ProvideIntegerData** method of the [**ConfigureModule object**](configuremodule-object.md) is called by Mergemod.dll to retrieve integer data from the client tool.</span></span>

<span data-ttu-id="0448b-105">Mergemod.dll proporciona el *nombre* de la entrada correspondiente en la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="0448b-105">Mergemod.dll provides the *Name* from the corresponding entry in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="0448b-106">La herramienta debe devolver S \_ correcto y proporcionar el entero de personalización correspondiente en *ConfigData*.</span><span class="sxs-lookup"><span data-stu-id="0448b-106">The tool should return S\_OK and provide the appropriate customization integer in *ConfigData*.</span></span>

<span data-ttu-id="0448b-107">Si la herramienta no proporciona ningún dato de configuración para este valor de *nombre* , la función debe devolver S \_ false.</span><span class="sxs-lookup"><span data-stu-id="0448b-107">If the tool does not provide any configuration data for this *Name* value, the function should return S\_FALSE.</span></span> <span data-ttu-id="0448b-108">En este caso Mergemod.dll omite el valor del argumento *ConfigData* y usa el valor predeterminado de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0448b-108">In this case Mergemod.dll ignores the value of the *ConfigData* argument and uses the Default value from the ModuleConfiguration table.</span></span>

## <a name="syntax"></a><span data-ttu-id="0448b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0448b-109">Syntax</span></span>


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a><span data-ttu-id="0448b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0448b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0448b-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="0448b-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="0448b-112">Nombre del elemento para el que se recuperan los datos.</span><span class="sxs-lookup"><span data-stu-id="0448b-112">Name of item for which data is being retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0448b-113">*ConfigData*</span><span class="sxs-lookup"><span data-stu-id="0448b-113">*ConfigData*</span></span> 
</dt> <dd>

<span data-ttu-id="0448b-114">Puntero al texto de personalización.</span><span class="sxs-lookup"><span data-stu-id="0448b-114">Pointer to customization text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0448b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0448b-115">Return value</span></span>

<span data-ttu-id="0448b-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0448b-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0448b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0448b-117">Remarks</span></span>

<span data-ttu-id="0448b-118">Es posible que el cliente no se llame más de una vez para cada registro de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="0448b-118">The client may be called no more than once for each record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="0448b-119">Tenga en cuenta que Mergemod.dll nunca realiza varias llamadas al cliente para el mismo valor "Name".</span><span class="sxs-lookup"><span data-stu-id="0448b-119">Note that Mergemod.dll never makes multiple calls to the client for the same "Name" value.</span></span> <span data-ttu-id="0448b-120">Si no hay ningún registro en la tabla ModuleSubstitution que usa la propiedad, una entrada de la tabla ModuleConfiguration no hace ninguna llamada al cliente.</span><span class="sxs-lookup"><span data-stu-id="0448b-120">If no record in the ModuleSubstitution table uses the property, an entry in the ModuleConfiguration table causes no calls to the client.</span></span>

### <a name="c"></a><span data-ttu-id="0448b-121">C++</span><span class="sxs-lookup"><span data-stu-id="0448b-121">C++</span></span>

<span data-ttu-id="0448b-122">Consulte [**función ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span><span class="sxs-lookup"><span data-stu-id="0448b-122">See [**ProvideIntegerData function**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).</span></span>

## <a name="requirements"></a><span data-ttu-id="0448b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0448b-123">Requirements</span></span>



| <span data-ttu-id="0448b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0448b-124">Requirement</span></span> | <span data-ttu-id="0448b-125">Value</span><span class="sxs-lookup"><span data-stu-id="0448b-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0448b-126">Versión</span><span class="sxs-lookup"><span data-stu-id="0448b-126">Version</span></span><br/> | <span data-ttu-id="0448b-127">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="0448b-127">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="0448b-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0448b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0448b-129"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="0448b-129"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="0448b-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0448b-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0448b-131"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0448b-131"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




