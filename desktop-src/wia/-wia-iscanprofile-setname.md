---
description: Establece el nombre descriptivo del perfil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'IScanProfile:: SetName (método) (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716061"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="a6e96-103">IScanProfile:: SetName (método)</span><span class="sxs-lookup"><span data-stu-id="a6e96-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="a6e96-104">Establece el nombre descriptivo del perfil.</span><span class="sxs-lookup"><span data-stu-id="a6e96-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6e96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6e96-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="a6e96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6e96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6e96-107">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a6e96-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6e96-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="a6e96-108">Type: **BSTR**</span></span>

<span data-ttu-id="a6e96-109">Nombre descriptivo del perfil.</span><span class="sxs-lookup"><span data-stu-id="a6e96-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6e96-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6e96-110">Return value</span></span>

<span data-ttu-id="a6e96-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a6e96-111">Type: **HRESULT**</span></span>

<span data-ttu-id="a6e96-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="a6e96-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a6e96-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6e96-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6e96-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6e96-114">Remarks</span></span>

<span data-ttu-id="a6e96-115">Este método es necesario porque el GUID de un perfil no se puede usar para mostrar el perfil de digitalización a un usuario.</span><span class="sxs-lookup"><span data-stu-id="a6e96-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="a6e96-116">Un usuario puede cambiar el nombre descriptivo de un perfil con el método [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="a6e96-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="a6e96-117">Los cambios en un perfil no se guardan en el disco hasta que la aplicación llama al método [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="a6e96-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="a6e96-118">Si dos aplicaciones crean objetos de Perfil de análisis a partir del mismo archivo XML y cada aplicación escribe cambios en su objeto, solo los cambios realizados por la aplicación que llama a [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last se guardan en el disco.</span><span class="sxs-lookup"><span data-stu-id="a6e96-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6e96-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6e96-119">Requirements</span></span>



| <span data-ttu-id="a6e96-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6e96-120">Requirement</span></span> | <span data-ttu-id="a6e96-121">Value</span><span class="sxs-lookup"><span data-stu-id="a6e96-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6e96-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6e96-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6e96-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a6e96-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a6e96-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6e96-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6e96-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6e96-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6e96-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6e96-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6e96-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6e96-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="a6e96-128">IDL</span><span class="sxs-lookup"><span data-stu-id="a6e96-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6e96-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6e96-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 




