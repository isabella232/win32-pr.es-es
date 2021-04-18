---
title: IWMPLibraryServices getLibraryByType, método
description: El método getLibraryByType devuelve una interfaz IWMPLibrary que representa la biblioteca que tiene el tipo y el índice especificados.
ms.assetid: 2507c764-a2cf-42f9-ad44-eaf040b78891
keywords:
- método getLibraryByType de Windows Media Player
- método getLibraryByType Windows Media Player, interfaz IWMPLibraryServices
- Interfaz IWMPLibraryServices Windows Media Player, método getLibraryByType
topic_type:
- apiref
api_name:
- IWMPLibraryServices.getLibraryByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d57fcc71f912fe1ee896ec893ea8f556eeb2277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671593"
---
# <a name="iwmplibraryservicesgetlibrarybytype-method"></a><span data-ttu-id="b105f-106">IWMPLibraryServices:: getLibraryByType (método)</span><span class="sxs-lookup"><span data-stu-id="b105f-106">IWMPLibraryServices::getLibraryByType method</span></span>

<span data-ttu-id="b105f-107">El método **getLibraryByType** devuelve una interfaz **IWMPLibrary** que representa la biblioteca que tiene el tipo y el índice especificados.</span><span class="sxs-lookup"><span data-stu-id="b105f-107">The **getLibraryByType** method returns an **IWMPLibrary** interface that represents the library that has the specified type and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b105f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b105f-108">Syntax</span></span>


```CSharp
public IWMPLibrary getLibraryByType(
  WMPLibraryType wmplt,
  System.Int32 lIndex
);
```


```VB

Public Function getLibraryByType( _
  ByVal wmplt As WMPLibraryType, _
  ByVal lIndex As System.Int32 _
) As IWMPLibrary
Implements IWMPLibraryServices.getLibraryByType
```





## <a name="parameters"></a><span data-ttu-id="b105f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b105f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b105f-110">*wmplt* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b105f-110">*wmplt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b105f-111">Un valor de la enumeración **WMPLib. WMPLibraryType** que especifica el tipo de biblioteca que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b105f-111">A value from the **WMPLib.WMPLibraryType** enumeration that specifies the type of library to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b105f-112">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b105f-112">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b105f-113">**System. Int32** que es el índice de la biblioteca que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="b105f-113">A **System.Int32** that is the index of the library to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b105f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b105f-114">Return value</span></span>

<span data-ttu-id="b105f-115">Una interfaz **WMPLib. IWMPLibrary** para la biblioteca que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="b105f-115">A **WMPLib.IWMPLibrary** interface for the library that is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="b105f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b105f-116">Remarks</span></span>

<span data-ttu-id="b105f-117">Solo hay una biblioteca local y las bibliotecas de discos solo están disponibles en CDs de datos y DVDs que contienen contenido multimedia.</span><span class="sxs-lookup"><span data-stu-id="b105f-117">There is only one local library, and disc libraries are available only on data CDs and DVDs that contain media content.</span></span>

## <a name="requirements"></a><span data-ttu-id="b105f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b105f-118">Requirements</span></span>



| <span data-ttu-id="b105f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b105f-119">Requirement</span></span> | <span data-ttu-id="b105f-120">Value</span><span class="sxs-lookup"><span data-stu-id="b105f-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b105f-121">Versión</span><span class="sxs-lookup"><span data-stu-id="b105f-121">Version</span></span><br/>   | <span data-ttu-id="b105f-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="b105f-122">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="b105f-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b105f-123">Namespace</span></span><br/> | <span data-ttu-id="b105f-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b105f-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b105f-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b105f-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b105f-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b105f-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b105f-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="b105f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b105f-128">**Interfaz IWMPLibrary (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b105f-128">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b105f-129">**Interfaz IWMPLibraryServices (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b105f-129">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b105f-130">**WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="b105f-130">**WMPLibraryType**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
</dt> </dl>

 

 





