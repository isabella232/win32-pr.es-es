---
description: Habilita las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de un cuenta Microsoft.
ms.assetid: 8b99eb84-c434-489a-b177-1e00f18d2dcc
title: Método NewWDEvents. PassportAuthenticate (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NewWDEvents.PassportAuthenticate
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 48e6cfbcbf525784fe33520702bbd9c05226f353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819043"
---
# <a name="newwdeventspassportauthenticate-method"></a><span data-ttu-id="7c976-103">NewWDEvents. PassportAuthenticate, método</span><span class="sxs-lookup"><span data-stu-id="7c976-103">NewWDEvents.PassportAuthenticate method</span></span>

<span data-ttu-id="7c976-104">Habilita las páginas del lado servidor hospedadas en un asistente para comprobar que el usuario se ha autenticado a través de un cuenta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7c976-104">Enables server-side pages hosted in a wizard to verify that the user has been authenticated through a Microsoft account.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c976-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c976-105">Syntax</span></span>


```JScript
bRetVal = NewWDEvents.PassportAuthenticate(
  bstrSignInUrl
)
```



## <a name="parameters"></a><span data-ttu-id="7c976-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c976-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c976-107">*bstrSignInUrl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7c976-107">*bstrSignInUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c976-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="7c976-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="7c976-109">Una cadena que contiene la dirección URL de una página web que redirige a la interfaz de usuario del registro de cuenta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7c976-109">A string containing the URL of a webpage that redirects to the Microsoft account log on UI.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c976-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c976-110">Return value</span></span>

<span data-ttu-id="7c976-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="7c976-111">Type: **Boolean**</span></span>

<span data-ttu-id="7c976-112">Establézcalo en **true** si la autenticación se realiza correctamente; de lo contrario, **false** .</span><span class="sxs-lookup"><span data-stu-id="7c976-112">Set to **true** if authentication succeeds, **false** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c976-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c976-113">Remarks</span></span>

<span data-ttu-id="7c976-114">Se puede llamar a este método incluso si un usuario ya ha iniciado sesión en un cuenta Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7c976-114">This method may be called even if a user is already logged on to a Microsoft account.</span></span> <span data-ttu-id="7c976-115">En ese caso, el método devuelve **true** sin mostrar el cuenta Microsoft la interfaz de usuario de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7c976-115">In that case, the method returns **true** without displaying the Microsoft account log on UI.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c976-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c976-116">Requirements</span></span>



| <span data-ttu-id="7c976-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c976-117">Requirement</span></span> | <span data-ttu-id="7c976-118">Value</span><span class="sxs-lookup"><span data-stu-id="7c976-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c976-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c976-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7c976-120">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7c976-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="7c976-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7c976-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7c976-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7c976-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7c976-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c976-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c976-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c976-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="7c976-125">IDL</span><span class="sxs-lookup"><span data-stu-id="7c976-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c976-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c976-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="7c976-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7c976-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c976-128"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="7c976-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
