---
description: Establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.
ms.assetid: f6da65d3-86dd-4fc8-b4c0-f7ddc8536d4e
ms.tgt_platform: multiple
title: '__SystemSecurity:: Set9XUserList (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.Set9XUserList
api_type:
- COM
api_location:
- all
ms.openlocfilehash: dd377da3adf55aef6a78576e1c978196f349f619
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697597"
---
# <a name="__systemsecurityset9xuserlist-method"></a><span data-ttu-id="2b5fb-103">\_\_SystemSecurity:: Set9XUserList (método)</span><span class="sxs-lookup"><span data-stu-id="2b5fb-103">\_\_SystemSecurity::Set9XUserList method</span></span>

<span data-ttu-id="2b5fb-104">El método **\_ \_ SystemSecurity:: Set9XUserList** establece los derechos de acceso remoto para una lista de usuarios individuales en equipos que ejecutan versiones obsoletas de Windows, donde el control de acceso a través de los descriptores de seguridad de Windows no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-104">The **\_\_SystemSecurity::Set9XUserList** method sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

<span data-ttu-id="2b5fb-105">La lista se especifica como una matriz de objetos incrustados, donde cada objeto es una instancia de la clase [**\_ \_ NTLMUser9X**](--ntlmuser9x.md) .</span><span class="sxs-lookup"><span data-stu-id="2b5fb-105">The list is specified as an array of embedded objects where each object is an instance of the [**\_\_NTLMUser9X**](--ntlmuser9x.md) class.</span></span> <span data-ttu-id="2b5fb-106">Esto funciona de forma similar al descriptor de seguridad, pero es más limitado.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-106">This functions similar to the security descriptor, but it is more limited.</span></span> <span data-ttu-id="2b5fb-107">No se admiten grupos y no hay ningún control sobre el acceso local, ya que el usuario local siempre tiene acceso completo.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-107">Groups are not supported and there is no control over local access, because the local user always has full access.</span></span> <span data-ttu-id="2b5fb-108">Se permiten las entradas de control de acceso (ACE) deny y allow y, debido a ello, el orden de ACE es importante en la lista de control de acceso discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="2b5fb-108">Both deny and allow access control entries (ACE) are permitted, and because of this, the ACE order is important in the discretionary access control list (DACL).</span></span> <span data-ttu-id="2b5fb-109">Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="2b5fb-109">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b5fb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b5fb-110">Syntax</span></span>


```C++
HRESULT Set9XUserList(
  [in] __NTLMUser9X ul[]
);
```



## <a name="parameters"></a><span data-ttu-id="2b5fb-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b5fb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5fb-112">*UL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b5fb-112">*ul* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b5fb-113">Matriz de usuarios.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-113">Array of users.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5fb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b5fb-114">Return value</span></span>

<span data-ttu-id="2b5fb-115">Este método devuelve un **valor HRESULT** que indica el estado de la llamada al método.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-115">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="2b5fb-116">En la lista siguiente se muestran los valores devueltos que son significativos para **Set9XUserList**.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-116">The following list lists the return values that are of significance to **Set9XUserList**.</span></span> <span data-ttu-id="2b5fb-117">En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2b5fb-117">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="2b5fb-118">Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="2b5fb-118">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="2b5fb-119">**WBEM \_ E \_ método \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="2b5fb-119">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="2b5fb-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="2b5fb-120">This method is not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2b5fb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b5fb-121">Requirements</span></span>



| <span data-ttu-id="2b5fb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b5fb-122">Requirement</span></span> | <span data-ttu-id="2b5fb-123">Value</span><span class="sxs-lookup"><span data-stu-id="2b5fb-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="2b5fb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b5fb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5fb-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b5fb-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="2b5fb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b5fb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5fb-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b5fb-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="2b5fb-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b5fb-128">Namespace</span></span><br/>                | <span data-ttu-id="2b5fb-129">todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="2b5fb-129">all WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="2b5fb-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b5fb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b5fb-131">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="2b5fb-131">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="2b5fb-132">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="2b5fb-132">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="2b5fb-133">**\_\_SystemSecurity:: obtiene**</span><span class="sxs-lookup"><span data-stu-id="2b5fb-133">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="2b5fb-134">**\_\_SystemSecurity:: establecido**</span><span class="sxs-lookup"><span data-stu-id="2b5fb-134">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="2b5fb-135">**ACE de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2b5fb-135">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="2b5fb-136">**SecurityDescriptor de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2b5fb-136">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="2b5fb-137">Proteger los espacios de nombres de WMI</span><span class="sxs-lookup"><span data-stu-id="2b5fb-137">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="2b5fb-138">Constantes de seguridad de WMI</span><span class="sxs-lookup"><span data-stu-id="2b5fb-138">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> </dl>

 

