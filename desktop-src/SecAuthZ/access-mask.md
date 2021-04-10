---
description: Define derechos estándar, específicos y genéricos. Estos derechos se usan en entradas de control de acceso (ACE) y son el medio principal para especificar el acceso solicitado o concedido a un objeto.
ms.assetid: f115ee54-3333-4109-8004-d71904a7a943
title: ACCESS_MASK (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d10d9e8db246c2705911cc57221400f40da014d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156296"
---
# <a name="access_mask"></a><span data-ttu-id="290b3-104">máscara de acceso \_</span><span class="sxs-lookup"><span data-stu-id="290b3-104">ACCESS\_MASK</span></span>

<span data-ttu-id="290b3-105">El tipo de datos de la **\_ máscara de acceso** es un valor **DWORD** que define derechos estándar, específicos y genéricos.</span><span class="sxs-lookup"><span data-stu-id="290b3-105">The **ACCESS\_MASK** data type is a **DWORD** value that defines standard, specific, and generic rights.</span></span> <span data-ttu-id="290b3-106">Estos derechos se usan en [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) y son el medio principal para especificar el acceso solicitado o concedido a un objeto.</span><span class="sxs-lookup"><span data-stu-id="290b3-106">These rights are used in [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) and are the primary means of specifying the requested or granted access to an object.</span></span>


```C++
typedef DWORD ACCESS_MASK;
typedef ACCESS_MASK* PACCESS_MASK;
```



## <a name="remarks"></a><span data-ttu-id="290b3-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="290b3-107">Remarks</span></span>

<span data-ttu-id="290b3-108">Los bits de este valor se asignan como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="290b3-108">The bits in this value are allocated as follows.</span></span>



| <span data-ttu-id="290b3-109">Bits</span><span class="sxs-lookup"><span data-stu-id="290b3-109">Bits</span></span>             | <span data-ttu-id="290b3-110">Significado</span><span class="sxs-lookup"><span data-stu-id="290b3-110">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="290b3-111">0 15</span><span class="sxs-lookup"><span data-stu-id="290b3-111">0 15</span></span><br/>  | <span data-ttu-id="290b3-112">Derechos específicos.</span><span class="sxs-lookup"><span data-stu-id="290b3-112">Specific rights.</span></span> <span data-ttu-id="290b3-113">Contiene la máscara de acceso específica del tipo de objeto asociado a la máscara.</span><span class="sxs-lookup"><span data-stu-id="290b3-113">Contains the access mask specific to the object type associated with the mask.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="290b3-114">16 23</span><span class="sxs-lookup"><span data-stu-id="290b3-114">16 23</span></span><br/> | <span data-ttu-id="290b3-115">Derechos estándar.</span><span class="sxs-lookup"><span data-stu-id="290b3-115">Standard rights.</span></span> <span data-ttu-id="290b3-116">Contiene los derechos de acceso estándar del objeto.</span><span class="sxs-lookup"><span data-stu-id="290b3-116">Contains the object's standard access rights.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="290b3-117">24</span><span class="sxs-lookup"><span data-stu-id="290b3-117">24</span></span><br/>    | <span data-ttu-id="290b3-118">Obtener acceso a la seguridad del sistema (**\_ \_ seguridad del sistema de acceso**).</span><span class="sxs-lookup"><span data-stu-id="290b3-118">Access system security (**ACCESS\_SYSTEM\_SECURITY**).</span></span> <span data-ttu-id="290b3-119">Se utiliza para indicar el acceso a una [*lista de control de acceso*](/windows/desktop/SecGloss/s-gly) (SACL) del sistema.</span><span class="sxs-lookup"><span data-stu-id="290b3-119">It is used to indicate access to a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="290b3-120">Este tipo de acceso requiere que el proceso de llamada tenga el privilegio de **\_ \_ nombre de seguridad se** (Administrar registro de auditoría y seguridad).</span><span class="sxs-lookup"><span data-stu-id="290b3-120">This type of access requires the calling process to have the **SE\_SECURITY\_NAME** (Manage auditing and security log) privilege.</span></span> <span data-ttu-id="290b3-121">Si esta marca se establece en la máscara de acceso de una ACE de acceso de auditoría (acceso correcto o incorrecto), se auditará el acceso a la SACL.</span><span class="sxs-lookup"><span data-stu-id="290b3-121">If this flag is set in the access mask of an audit access ACE (successful or unsuccessful access), the SACL access will be audited.</span></span><br/> |
| <span data-ttu-id="290b3-122">25</span><span class="sxs-lookup"><span data-stu-id="290b3-122">25</span></span><br/>    | <span data-ttu-id="290b3-123">Máximo permitido (**máximo \_ permitido**).</span><span class="sxs-lookup"><span data-stu-id="290b3-123">Maximum allowed (**MAXIMUM\_ALLOWED**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="290b3-124">26 27</span><span class="sxs-lookup"><span data-stu-id="290b3-124">26 27</span></span><br/> | <span data-ttu-id="290b3-125">Reservado.</span><span class="sxs-lookup"><span data-stu-id="290b3-125">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="290b3-126">28</span><span class="sxs-lookup"><span data-stu-id="290b3-126">28</span></span><br/>    | <span data-ttu-id="290b3-127">Genérico All (**genérico \_ All**).</span><span class="sxs-lookup"><span data-stu-id="290b3-127">Generic all (**GENERIC\_ALL**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="290b3-128">29</span><span class="sxs-lookup"><span data-stu-id="290b3-128">29</span></span><br/>    | <span data-ttu-id="290b3-129">Ejecución genérica (**\_ ejecución genérica**).</span><span class="sxs-lookup"><span data-stu-id="290b3-129">Generic execute (**GENERIC\_EXECUTE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="290b3-130">30</span><span class="sxs-lookup"><span data-stu-id="290b3-130">30</span></span><br/>    | <span data-ttu-id="290b3-131">Escritura genérica (**\_ escritura genérica**).</span><span class="sxs-lookup"><span data-stu-id="290b3-131">Generic write (**GENERIC\_WRITE**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="290b3-132">31</span><span class="sxs-lookup"><span data-stu-id="290b3-132">31</span></span><br/>    | <span data-ttu-id="290b3-133">Lectura genérica (**\_ lectura genérica**).</span><span class="sxs-lookup"><span data-stu-id="290b3-133">Generic read (**GENERIC\_READ**).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

<span data-ttu-id="290b3-134">Los bits de derechos estándar, de 16 a 23, contienen los derechos de acceso estándar del objeto y pueden ser una combinación de las siguientes marcas predefinidas.</span><span class="sxs-lookup"><span data-stu-id="290b3-134">Standard rights bits, 16 to 23, contain the object's standard access rights and can be a combination of the following predefined flags.</span></span>



| <span data-ttu-id="290b3-135">bit</span><span class="sxs-lookup"><span data-stu-id="290b3-135">Bit</span></span>           | <span data-ttu-id="290b3-136">Marca</span><span class="sxs-lookup"><span data-stu-id="290b3-136">Flag</span></span>                         | <span data-ttu-id="290b3-137">Significado</span><span class="sxs-lookup"><span data-stu-id="290b3-137">Meaning</span></span>                                                                                                                                                                                                                                  |
|---------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="290b3-138">16</span><span class="sxs-lookup"><span data-stu-id="290b3-138">16</span></span><br/> | <span data-ttu-id="290b3-139">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="290b3-139">**DELETE**</span></span><br/>        | <span data-ttu-id="290b3-140">Elimine el acceso.</span><span class="sxs-lookup"><span data-stu-id="290b3-140">Delete access.</span></span><br/>                                                                                                                                                                                                                |
| <span data-ttu-id="290b3-141">17</span><span class="sxs-lookup"><span data-stu-id="290b3-141">17</span></span><br/> | <span data-ttu-id="290b3-142">**CONTROL de lectura \_**</span><span class="sxs-lookup"><span data-stu-id="290b3-142">**READ\_CONTROL**</span></span><br/> | <span data-ttu-id="290b3-143">Acceso de lectura al propietario, grupo y [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL) del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="290b3-143">Read access to the owner, group, and [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) of the security descriptor.</span></span><br/> |
| <span data-ttu-id="290b3-144">18</span><span class="sxs-lookup"><span data-stu-id="290b3-144">18</span></span><br/> | <span data-ttu-id="290b3-145">**ESCRIBIR \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="290b3-145">**WRITE\_DAC**</span></span><br/>    | <span data-ttu-id="290b3-146">Acceso de escritura a la DACL.</span><span class="sxs-lookup"><span data-stu-id="290b3-146">Write access to the DACL.</span></span><br/>                                                                                                                                                                                                     |
| <span data-ttu-id="290b3-147">19</span><span class="sxs-lookup"><span data-stu-id="290b3-147">19</span></span><br/> | <span data-ttu-id="290b3-148">**propietario de escritura \_**</span><span class="sxs-lookup"><span data-stu-id="290b3-148">**WRITE\_OWNER**</span></span><br/>  | <span data-ttu-id="290b3-149">Acceso de escritura al propietario.</span><span class="sxs-lookup"><span data-stu-id="290b3-149">Write access to owner.</span></span><br/>                                                                                                                                                                                                        |
| <span data-ttu-id="290b3-150">20</span><span class="sxs-lookup"><span data-stu-id="290b3-150">20</span></span><br/> | <span data-ttu-id="290b3-151">**SYNCHRONIZE**</span><span class="sxs-lookup"><span data-stu-id="290b3-151">**SYNCHRONIZE**</span></span><br/>   | <span data-ttu-id="290b3-152">Sincronizar el acceso.</span><span class="sxs-lookup"><span data-stu-id="290b3-152">Synchronize access.</span></span><br/>                                                                                                                                                                                                           |



 

<span data-ttu-id="290b3-153">Las siguientes constantes definidas en Winnt. h representan los derechos de acceso específicos y estándar.</span><span class="sxs-lookup"><span data-stu-id="290b3-153">The following constants defined in Winnt.h represent the specific and standard access rights.</span></span>


```C++
#define DELETE                           (0x00010000L)
#define READ_CONTROL                     (0x00020000L)
#define WRITE_DAC                        (0x00040000L)
#define WRITE_OWNER                      (0x00080000L)
#define SYNCHRONIZE                      (0x00100000L)

#define STANDARD_RIGHTS_REQUIRED         (0x000F0000L)

#define STANDARD_RIGHTS_READ             (READ_CONTROL)
#define STANDARD_RIGHTS_WRITE            (READ_CONTROL)
#define STANDARD_RIGHTS_EXECUTE          (READ_CONTROL)

#define STANDARD_RIGHTS_ALL              (0x001F0000L)

#define SPECIFIC_RIGHTS_ALL              (0x0000FFFFL)
```



## <a name="requirements"></a><span data-ttu-id="290b3-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="290b3-154">Requirements</span></span>



| <span data-ttu-id="290b3-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="290b3-155">Requirement</span></span> | <span data-ttu-id="290b3-156">Value</span><span class="sxs-lookup"><span data-stu-id="290b3-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="290b3-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="290b3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="290b3-158">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="290b3-158">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="290b3-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="290b3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="290b3-160">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="290b3-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="290b3-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="290b3-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="290b3-162"><dt>Winnt. h (incluye Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="290b3-162"><dt>Winnt.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="290b3-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="290b3-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="290b3-164">Control de acceso</span><span class="sxs-lookup"><span data-stu-id="290b3-164">Access Control</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="290b3-165">Estructuras de Access Control básicas</span><span class="sxs-lookup"><span data-stu-id="290b3-165">Basic Access Control Structures</span></span>](authorization-structures.md)
</dt> <dt>

[<span data-ttu-id="290b3-166">Derechos de acceso y máscaras de acceso</span><span class="sxs-lookup"><span data-stu-id="290b3-166">Access Rights and Access Masks</span></span>](access-rights-and-access-masks.md)
</dt> <dt>

[<span data-ttu-id="290b3-167">**\_asignación genérica**</span><span class="sxs-lookup"><span data-stu-id="290b3-167">**GENERIC\_MAPPING**</span></span>](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)
</dt> </dl>

 

