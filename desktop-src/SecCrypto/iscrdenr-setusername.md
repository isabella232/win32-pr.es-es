---
description: Especifica el nombre del usuario en cuyo nombre se ha diseñado la inscripción de certificados.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'ISCrdEnr:: setUserName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688674"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="440b2-103">ISCrdEnr:: setUserName (método)</span><span class="sxs-lookup"><span data-stu-id="440b2-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="440b2-104">El método **setUserName** especifica el nombre del usuario en cuyo nombre se ha diseñado la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="440b2-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="440b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="440b2-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="440b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="440b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="440b2-107">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="440b2-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="440b2-108">Este valor debe ser el \_ \_ \_ nombre de UPN de inscripción PPAC (definido como 1) o \_ \_ \_ el nombre compatible con el SAM de inscripción de Sam \_ (definido como 2).</span><span class="sxs-lookup"><span data-stu-id="440b2-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="440b2-109">Establezca este valor en PPACd \_ ENROLL \_ UPN \_ Name, si el nombre especificado en *bstrUserName* es el nombre de la entidad de seguridad universal del usuario, por ejemplo, " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="440b2-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="440b2-110">El nombre de UPN del usuario debe corresponder a un nombre de administrador de acceso de seguridad (SAM) existente.</span><span class="sxs-lookup"><span data-stu-id="440b2-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="440b2-111">Establezca este valor en el \_ \_ nombre compatible con el SAM de inscripción \_ \_ , si el nombre especificado en *BSTRUSERNAME* es el nombre del SAM del usuario con el formato "usuario del dominio \\ ".</span><span class="sxs-lookup"><span data-stu-id="440b2-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="440b2-112">*bstrUserName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="440b2-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="440b2-113">Nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="440b2-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="440b2-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="440b2-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="440b2-115">VB</span><span class="sxs-lookup"><span data-stu-id="440b2-115">VB</span></span>

<span data-ttu-id="440b2-116">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="440b2-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="440b2-117">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="440b2-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="440b2-118">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="440b2-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="440b2-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="440b2-119">Remarks</span></span>

<span data-ttu-id="440b2-120">Llame a este método para especificar el nombre de usuario para el que se va a emitir la [*tarjeta inteligente*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="440b2-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="440b2-121">Una alternativa a **setUserName** es [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="440b2-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="440b2-122">Una vez que se ha especificado un nombre de usuario, su valor se puede recuperar llamando a [**getUserName**](iscrdenr-getusername.md).</span><span class="sxs-lookup"><span data-stu-id="440b2-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="440b2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="440b2-123">Requirements</span></span>



| <span data-ttu-id="440b2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="440b2-124">Requirement</span></span> | <span data-ttu-id="440b2-125">Value</span><span class="sxs-lookup"><span data-stu-id="440b2-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="440b2-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="440b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="440b2-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="440b2-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="440b2-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="440b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="440b2-129">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="440b2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="440b2-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="440b2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="440b2-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="440b2-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="440b2-132">IID</span><span class="sxs-lookup"><span data-stu-id="440b2-132">IID</span></span><br/>                      | <span data-ttu-id="440b2-133">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="440b2-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="440b2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="440b2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440b2-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="440b2-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="440b2-136">**ISCrdEnr:: getUserName**</span><span class="sxs-lookup"><span data-stu-id="440b2-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="440b2-137">**ISCrdEnr:: resetuser**</span><span class="sxs-lookup"><span data-stu-id="440b2-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="440b2-138">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="440b2-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
