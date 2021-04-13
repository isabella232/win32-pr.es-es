---
title: Punto de entrada de VirtualChannelGetInstance
description: Se llama para que el complemento cree una instancia de la interfaz IWTSPlugin para todos los complementos implementados por el archivo DLL.
ms.assetid: B81BD61E-1F43-42C9-8839-30F4F4C3973C
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de punto de entrada de VirtualChannelGetInstance
topic_type:
- apiref
api_name:
- VirtualChannelGetInstance
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 535ebdc8928cceb282dd62de56f8c6fbadc94e90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422119"
---
# <a name="virtualchannelgetinstance-entry-point"></a><span data-ttu-id="612c2-104">Punto de entrada de VirtualChannelGetInstance</span><span class="sxs-lookup"><span data-stu-id="612c2-104">VirtualChannelGetInstance entry point</span></span>

<span data-ttu-id="612c2-105">Se llama para que el complemento cree una instancia de la interfaz [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) para todos los complementos implementados por el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="612c2-105">Called to have the plug-in create an instance of the [**IWTSPlugin**](/windows/desktop/api/TsVirtualChannels/nn-tsvirtualchannels-iwtsplugin) interface for all plug-ins implemented by the DLL.</span></span>

> [!Note]
>
> <span data-ttu-id="612c2-106">Esta función se implementa mediante el complemento y se debe exportar por nombre de modo que una aplicación pueda usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a la función.</span><span class="sxs-lookup"><span data-stu-id="612c2-106">This function is implemented by the plug-in and must be exported by name such that an application can use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to the function.</span></span>
>
> <span data-ttu-id="612c2-107">El prototipo de esta función no está incluido en ningún archivo de encabezado público, por lo que debe declararlo exactamente como se muestra.</span><span class="sxs-lookup"><span data-stu-id="612c2-107">The prototype for this function is not contained in any public header file, so you must declare it exactly as shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="612c2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="612c2-108">Syntax</span></span>


```C++
HRESULT VCAPITYPE VirtualChannelGetInstance(
  _In_    REFIID refiid,
  _Inout_ ULONG  *pNumObjs,
  _Out_   VOID   **ppObjArray
);
```



## <a name="parameters"></a><span data-ttu-id="612c2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="612c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="612c2-110">*REFIID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="612c2-110">*refiid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="612c2-111">Especifica el tipo de interfaz que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="612c2-111">Specifies the type of interface to return.</span></span> <span data-ttu-id="612c2-112">Debe ser **IID \_ IWTSPlugin**.</span><span class="sxs-lookup"><span data-stu-id="612c2-112">This must be **IID\_IWTSPlugin**.</span></span>

</dd> <dt>

<span data-ttu-id="612c2-113">*pNumObjs* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="612c2-113">*pNumObjs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="612c2-114">Dirección de una variable **ULong** que recibe el número de interfaces recuperadas.</span><span class="sxs-lookup"><span data-stu-id="612c2-114">The address of a **ULONG** variable that receives the number of interfaces retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="612c2-115">*ppObjArray* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="612c2-115">*ppObjArray* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="612c2-116">Dirección de una matriz de punteros que recibe los punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="612c2-116">The address of an array of pointers that receives the interface pointers.</span></span> <span data-ttu-id="612c2-117">Si este parámetro es **null**, la implementación debe colocar el número de complementos implementados por el archivo dll en el parámetro *pNumObjs* .</span><span class="sxs-lookup"><span data-stu-id="612c2-117">If this parameter is **NULL**, the implementation must put the number of plug-ins implemented by the DLL in the *pNumObjs* parameter.</span></span> <span data-ttu-id="612c2-118">Esto permite al llamador asignar la matriz de tamaño adecuada para *ppObjArray*.</span><span class="sxs-lookup"><span data-stu-id="612c2-118">This allows the caller to allocate the proper size array for *ppObjArray*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="612c2-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="612c2-119">Return value</span></span>

<span data-ttu-id="612c2-120">Si este punto de entrada se realiza correctamente, devuelve **S \_ correctos**.</span><span class="sxs-lookup"><span data-stu-id="612c2-120">If this entry point succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="612c2-121">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="612c2-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="612c2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="612c2-122">Requirements</span></span>



| <span data-ttu-id="612c2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="612c2-123">Requirement</span></span> | <span data-ttu-id="612c2-124">Value</span><span class="sxs-lookup"><span data-stu-id="612c2-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="612c2-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="612c2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="612c2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="612c2-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="612c2-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="612c2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="612c2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="612c2-128">Windows Server 2008</span></span><br/> |



 

