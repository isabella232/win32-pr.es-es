---
description: Recupera el nombre del usuario en cuyo nombre está diseñada la inscripción de certificados.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'ISCrdEnr:: getUserName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361300"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="46e31-103">ISCrdEnr:: getUserName (método)</span><span class="sxs-lookup"><span data-stu-id="46e31-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="46e31-104">El método **getUserName** recupera el nombre del usuario en cuyo nombre está dirigida la inscripción del certificado.</span><span class="sxs-lookup"><span data-stu-id="46e31-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="46e31-105">Antes de llamar a este método, debe especificar el nombre de usuario en una llamada a [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md) o [**ISCrdEnr:: setUserName**](iscrdenr-setusername.md).</span><span class="sxs-lookup"><span data-stu-id="46e31-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="46e31-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46e31-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="46e31-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46e31-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46e31-108">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="46e31-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46e31-109">Este valor debe ser cero (0), \_ nombre de UPN de inscripción PPAC \_ \_ o \_ \_ \_ nombre compatible con el SAM de inscripción \_ .</span><span class="sxs-lookup"><span data-stu-id="46e31-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="46e31-110">Si este valor es PPAC \_ ENROLL \_ UPN \_ Name, **GetUserName** devuelve el nombre principal universal (UPN) del usuario, como " someone@example.com ".</span><span class="sxs-lookup"><span data-stu-id="46e31-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="46e31-111">Si este valor es PPAC \_ inscribir \_ \_ el nombre compatible con Sam \_ , el método devuelve el nombre del administrador de acceso de seguridad (SAM) del usuario con el formato "dominio \\ usuario".</span><span class="sxs-lookup"><span data-stu-id="46e31-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="46e31-112">Si este valor es cero, el método devuelve el nombre UPN del usuario, si existe.</span><span class="sxs-lookup"><span data-stu-id="46e31-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="46e31-113">Si el usuario no tiene un nombre UPN, el método devuelve el nombre del SAM del usuario.</span><span class="sxs-lookup"><span data-stu-id="46e31-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="46e31-114">*pbstrUserName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="46e31-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46e31-115">Puntero a una cadena que devuelve el nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="46e31-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46e31-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46e31-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="46e31-117">C++</span><span class="sxs-lookup"><span data-stu-id="46e31-117">C++</span></span>

<span data-ttu-id="46e31-118">Si el método se ejecuta correctamente, el método devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="46e31-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="46e31-119">Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error.</span><span class="sxs-lookup"><span data-stu-id="46e31-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="46e31-120">Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="46e31-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="46e31-121">VB</span><span class="sxs-lookup"><span data-stu-id="46e31-121">VB</span></span>

<span data-ttu-id="46e31-122">Cadena que representa el nombre del usuario.</span><span class="sxs-lookup"><span data-stu-id="46e31-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="46e31-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46e31-123">Remarks</span></span>

<span data-ttu-id="46e31-124">Puede especificar el nombre del usuario al que se emite la [*tarjeta inteligente*](../secgloss/s-gly.md) llamando a [**ISCrdEnr:: setUserName**](iscrdenr-setusername.md) o [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="46e31-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="46e31-125">Una vez que se ha especificado un nombre de usuario, su valor se puede recuperar llamando a **getUserName**.</span><span class="sxs-lookup"><span data-stu-id="46e31-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46e31-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46e31-126">Requirements</span></span>



| <span data-ttu-id="46e31-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="46e31-127">Requirement</span></span> | <span data-ttu-id="46e31-128">Value</span><span class="sxs-lookup"><span data-stu-id="46e31-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46e31-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e31-129">Minimum supported client</span></span><br/> | <span data-ttu-id="46e31-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="46e31-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="46e31-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46e31-131">Minimum supported server</span></span><br/> | <span data-ttu-id="46e31-132">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="46e31-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46e31-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46e31-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46e31-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46e31-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="46e31-135">IID</span><span class="sxs-lookup"><span data-stu-id="46e31-135">IID</span></span><br/>                      | <span data-ttu-id="46e31-136">IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="46e31-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="46e31-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="46e31-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46e31-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="46e31-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="46e31-139">**ISCrdEnr:: resetuser**</span><span class="sxs-lookup"><span data-stu-id="46e31-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="46e31-140">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="46e31-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="46e31-141">**ISCrdEnr::setUserName**</span><span class="sxs-lookup"><span data-stu-id="46e31-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
