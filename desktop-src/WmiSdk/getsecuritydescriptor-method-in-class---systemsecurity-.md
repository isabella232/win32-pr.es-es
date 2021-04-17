---
description: Obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado. El descriptor de seguridad se devuelve como una instancia de \_ \_ SecurityDescriptor.
ms.assetid: b031af45-9237-434d-91db-69222306c615
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 7aece0a50678689141de9b9a38a014414578de3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706759"
---
# <a name="getsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="1d97a-104">Método GetSecurityDescriptor de la \_ \_ clase SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="1d97a-104">GetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="1d97a-105">El método **GetSecurityDescriptor** obtiene el descriptor de seguridad que controla el acceso al espacio de nombres WMI al que está conectado.</span><span class="sxs-lookup"><span data-stu-id="1d97a-105">The **GetSecurityDescriptor** method gets the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="1d97a-106">El descriptor de seguridad se devuelve como una instancia de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="1d97a-106">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="1d97a-107">Para obtener más información, consulte [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1d97a-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1d97a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1d97a-108">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] __SystemSecurity Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="1d97a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1d97a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d97a-110">*Descriptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1d97a-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d97a-111">Descriptor de seguridad asociado al espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="1d97a-111">The security descriptor associated with the WMI namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d97a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1d97a-112">Return value</span></span>

<span data-ttu-id="1d97a-113">Devuelve uno de los valores enumerados en la lista siguiente o un valor diferente para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1d97a-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="1d97a-114">Para obtener más información, vea [códigos de retorno de WMI](wmi-return-codes.md) o [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1d97a-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="1d97a-115">**0**</span><span class="sxs-lookup"><span data-stu-id="1d97a-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1d97a-116">Finalización correcta.</span><span class="sxs-lookup"><span data-stu-id="1d97a-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="1d97a-117">**2**</span><span class="sxs-lookup"><span data-stu-id="1d97a-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1d97a-118">El usuario no tiene acceso a la información solicitada.</span><span class="sxs-lookup"><span data-stu-id="1d97a-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="1d97a-119">**8**</span><span class="sxs-lookup"><span data-stu-id="1d97a-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1d97a-120">Error desconocido.</span><span class="sxs-lookup"><span data-stu-id="1d97a-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="1d97a-121">**9**</span><span class="sxs-lookup"><span data-stu-id="1d97a-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1d97a-122">El usuario no tiene los privilegios adecuados para ejecutar el método.</span><span class="sxs-lookup"><span data-stu-id="1d97a-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="1d97a-123">**21**</span><span class="sxs-lookup"><span data-stu-id="1d97a-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1d97a-124">Un parámetro especificado en la llamada al método no es válido.</span><span class="sxs-lookup"><span data-stu-id="1d97a-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d97a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1d97a-125">Remarks</span></span>

<span data-ttu-id="1d97a-126">La instancia de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa un tipo de datos de [**\_ \_ control de descriptor de seguridad**](/windows/desktop/SecAuthZ/security-descriptor-control) y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) y una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="1d97a-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="1d97a-127">Para obtener más información, vea [listas de Access Control](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="1d97a-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="1d97a-128">Si no se concede o habilita **SeSecurityPrivilege** cuando se obtiene un descriptor de seguridad, solo se devuelve la DACL en el descriptor de seguridad devuelto.</span><span class="sxs-lookup"><span data-stu-id="1d97a-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="1d97a-129">Para obtener más información, vea [**constantes de privilegios**](privilege-constants.md) y [ejecutar operaciones con privilegios](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="1d97a-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d97a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d97a-130">Requirements</span></span>



| <span data-ttu-id="1d97a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d97a-131">Requirement</span></span> | <span data-ttu-id="1d97a-132">Value</span><span class="sxs-lookup"><span data-stu-id="1d97a-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1d97a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d97a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1d97a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d97a-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1d97a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1d97a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1d97a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d97a-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="1d97a-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1d97a-137">Namespace</span></span><br/>                | <span data-ttu-id="1d97a-138">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="1d97a-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="1d97a-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1d97a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d97a-140">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="1d97a-140">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="1d97a-141">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="1d97a-141">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

