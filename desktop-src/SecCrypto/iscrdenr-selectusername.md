---
description: Muestra una interfaz de usuario seleccionada que permite seleccionar un nombre de usuario.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'ISCrdEnr:: selectUserName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668332"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="81d17-103">ISCrdEnr:: selectUserName (método)</span><span class="sxs-lookup"><span data-stu-id="81d17-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="81d17-104">El método **selectUserName** muestra una interfaz de **usuario** seleccionada que permite seleccionar un nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="81d17-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="81d17-105">El nombre de usuario se aplica al usuario en cuyo nombre está diseñada la inscripción de certificado.</span><span class="sxs-lookup"><span data-stu-id="81d17-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="81d17-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81d17-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="81d17-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81d17-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81d17-108">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="81d17-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81d17-109">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="81d17-109">Reserved for future use.</span></span> <span data-ttu-id="81d17-110">Establezca este valor en cero.</span><span class="sxs-lookup"><span data-stu-id="81d17-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81d17-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81d17-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="81d17-112">VB</span><span class="sxs-lookup"><span data-stu-id="81d17-112">VB</span></span>

<span data-ttu-id="81d17-113">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="81d17-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="81d17-114">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="81d17-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="81d17-115">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="81d17-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="81d17-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="81d17-116">Remarks</span></span>

<span data-ttu-id="81d17-117">Use este método para seleccionar el nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="81d17-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="81d17-118">Una vez que se ha seleccionado un nombre de usuario, su valor se puede recuperar llamando al método [**ISCrdEnr:: getUserName**](iscrdenr-getusername.md) .</span><span class="sxs-lookup"><span data-stu-id="81d17-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="81d17-119">Una alternativa al uso de la interfaz ' Select User ' consiste en especificar un usuario mediante una llamada al método [**ISCrdEnr:: setUserName**](iscrdenr-setusername.md) .</span><span class="sxs-lookup"><span data-stu-id="81d17-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="81d17-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81d17-120">Requirements</span></span>



| <span data-ttu-id="81d17-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="81d17-121">Requirement</span></span> | <span data-ttu-id="81d17-122">Value</span><span class="sxs-lookup"><span data-stu-id="81d17-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81d17-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81d17-123">Minimum supported client</span></span><br/> | <span data-ttu-id="81d17-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81d17-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="81d17-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81d17-125">Minimum supported server</span></span><br/> | <span data-ttu-id="81d17-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="81d17-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="81d17-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81d17-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81d17-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81d17-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="81d17-129">IID</span><span class="sxs-lookup"><span data-stu-id="81d17-129">IID</span></span><br/>                      | <span data-ttu-id="81d17-130">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="81d17-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="81d17-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="81d17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81d17-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="81d17-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="81d17-133">**ISCrdEnr:: getUserName**</span><span class="sxs-lookup"><span data-stu-id="81d17-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="81d17-134">**ISCrdEnr:: resetuser**</span><span class="sxs-lookup"><span data-stu-id="81d17-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="81d17-135">**ISCrdEnr::setUserName**</span><span class="sxs-lookup"><span data-stu-id="81d17-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




