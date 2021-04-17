---
description: Obtiene los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.
ms.assetid: 79a596db-5f85-4664-8989-f309286eca0d
ms.tgt_platform: multiple
title: '__SystemSecurity:: Get9XUserList (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Get9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: 521f2fe489089d486480c138293ebea39ca6f105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659943"
---
# <a name="__systemsecurityget9xuserlist-method"></a><span data-ttu-id="6abd4-103">\_\_SystemSecurity:: Get9XUserList (método)</span><span class="sxs-lookup"><span data-stu-id="6abd4-103">\_\_SystemSecurity::Get9XUserList method</span></span>

<span data-ttu-id="6abd4-104">El método [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) obtiene los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.</span><span class="sxs-lookup"><span data-stu-id="6abd4-104">The [**\_\_SystemSecurity::Set9XUserList**](--systemsecurity-set9xuserlist.md) method gets the remote access rights for a list of individual users on computers running obsolete versions of Windows , where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="6abd4-105">Esto funciona de forma similar al descriptor de seguridad, pero es más limitado.</span><span class="sxs-lookup"><span data-stu-id="6abd4-105">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="6abd4-106">No se admiten grupos y no hay ningún control sobre el acceso local, ya que el usuario local siempre tiene acceso completo.</span><span class="sxs-lookup"><span data-stu-id="6abd4-106">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="6abd4-107">Se permiten las entradas de control de acceso (ACE) deny y allow y, debido a ello, el orden de ACE es importante en la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="6abd4-107">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="6abd4-108">Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="6abd4-108">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="6abd4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6abd4-109">Syntax</span></span>


```C++
HRESULT Get9XUserList(
  [out] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="6abd4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6abd4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6abd4-111">*UL* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6abd4-111">*ul* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6abd4-112">Matriz de usuarios.</span><span class="sxs-lookup"><span data-stu-id="6abd4-112">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6abd4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6abd4-113">Return value</span></span>

<span data-ttu-id="6abd4-114">Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="6abd4-114">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="6abd4-115">En la lista siguiente se muestran los valores devueltos que son significativos para **Get9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="6abd4-115">The following list lists the return values that are of significance to **Get9XUserList**.</span></span> <span data-ttu-id="6abd4-116">En el caso de las aplicaciones de scripting y Visual Basic, el resultado puede ser [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6abd4-116">For scripting and Visual Basic applications, the result can be [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="6abd4-117">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="6abd4-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="6abd4-118">**WBEM \_ E \_ método \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="6abd4-118">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="6abd4-119">Este método no se admite en las versiones compatibles de Windows.</span><span class="sxs-lookup"><span data-stu-id="6abd4-119">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6abd4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6abd4-120">Requirements</span></span>



| <span data-ttu-id="6abd4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6abd4-121">Requirement</span></span> | <span data-ttu-id="6abd4-122">Value</span><span class="sxs-lookup"><span data-stu-id="6abd4-122">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="6abd4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6abd4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6abd4-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6abd4-124">Windows Vista</span></span><br/>       |
| <span data-ttu-id="6abd4-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6abd4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6abd4-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6abd4-126">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="6abd4-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6abd4-127">Namespace</span></span><br/>                | <span data-ttu-id="6abd4-128">todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="6abd4-128">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="6abd4-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6abd4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6abd4-130">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="6abd4-130">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="6abd4-131">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="6abd4-131">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="6abd4-132">**\_\_SystemSecurity:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="6abd4-132">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="6abd4-133">**\_\_SystemSecurity:: establecido**</span><span class="sxs-lookup"><span data-stu-id="6abd4-133">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="6abd4-134">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="6abd4-134">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="6abd4-135">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="6abd4-135">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="6abd4-136">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="6abd4-136">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="6abd4-137">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="6abd4-137">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

