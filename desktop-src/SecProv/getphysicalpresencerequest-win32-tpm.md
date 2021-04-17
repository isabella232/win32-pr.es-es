---
description: Devuelve la operación de presencia física de TPM pendiente. Use el método SetPhysicalPresenceRequest para solicitar una operación.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Método GetPhysicalPresenceRequest de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688155"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="780ec-104">Método GetPhysicalPresenceRequest de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="780ec-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="780ec-105">El método **GetPhysicalPresenceRequest** de la clase [**Win32 \_ TPM**](win32-tpm.md) devuelve la operación de presencia física de TPM pendiente.</span><span class="sxs-lookup"><span data-stu-id="780ec-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="780ec-106">Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.</span><span class="sxs-lookup"><span data-stu-id="780ec-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="780ec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="780ec-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="780ec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="780ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="780ec-109">*Solicitud* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="780ec-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="780ec-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="780ec-110">Type: **uint32**</span></span>

<span data-ttu-id="780ec-111">Valor que especifica la operación de presencia física del TPM pendiente.</span><span class="sxs-lookup"><span data-stu-id="780ec-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="780ec-112">Value</span><span class="sxs-lookup"><span data-stu-id="780ec-112">Value</span></span></th>
<th><span data-ttu-id="780ec-113">Significado</span><span class="sxs-lookup"><span data-stu-id="780ec-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-114"><dt>0,1</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-115">Ninguna solicitud.</span><span class="sxs-lookup"><span data-stu-id="780ec-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-117">Habilite el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-117">Enable the TPM.</span></span><br/> <span data-ttu-id="780ec-118">Esta operación se invierte en la operación 2.</span><span class="sxs-lookup"><span data-stu-id="780ec-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="780ec-119">Para obtener más información, consulte estos métodos relacionados que no implican la presencia física:</span><span class="sxs-lookup"><span data-stu-id="780ec-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="780ec-120"><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></span><span class="sxs-lookup"><span data-stu-id="780ec-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="780ec-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="780ec-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-123">Deshabilite TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-123">Disable the TPM.</span></span><br/> <span data-ttu-id="780ec-124">Esta operación se invierte en la operación 1.</span><span class="sxs-lookup"><span data-stu-id="780ec-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="780ec-125">Para obtener más información, vea este método relacionado que no implica la presencia física: <a href="disable-win32-tpm.md"><strong>deshabilitar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="780ec-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-126"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-127">Active el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-127">Activate the TPM.</span></span><br/> <span data-ttu-id="780ec-128">Esta operación se invierte en la operación 4.</span><span class="sxs-lookup"><span data-stu-id="780ec-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-130">Desactive el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="780ec-131">Esta operación se invierte en la operación 3.</span><span class="sxs-lookup"><span data-stu-id="780ec-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-132"><dt>5</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-133">Borre el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-133">Clear the TPM.</span></span><br/> <span data-ttu-id="780ec-134">Esta operación no se puede revertir.</span><span class="sxs-lookup"><span data-stu-id="780ec-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="780ec-135">Para obtener más información, consulte este método relacionado que no implica la presencia física: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="780ec-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-136"><dt>1,8</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-137">Habilitar y activar el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="780ec-138">Esta operación se invierte en la operación 7.</span><span class="sxs-lookup"><span data-stu-id="780ec-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-140">Desactivar y deshabilitar TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="780ec-141">Esta operación se invierte en la operación 6.</span><span class="sxs-lookup"><span data-stu-id="780ec-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-142"><dt>203</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-143">Permitir la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="780ec-144">Esta operación se invierte en la operación 9.</span><span class="sxs-lookup"><span data-stu-id="780ec-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-145"><dt>9</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-146">Impedir la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="780ec-147">Esta operación se invierte en la operación 8.</span><span class="sxs-lookup"><span data-stu-id="780ec-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-148"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-149">Habilitar, activar y permitir la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="780ec-150">Esta operación se invierte en la operación 11.</span><span class="sxs-lookup"><span data-stu-id="780ec-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-151"><dt>279</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-152">Desactive, deshabilite y evite la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="780ec-153">Esta operación se invierte en la operación 10.</span><span class="sxs-lookup"><span data-stu-id="780ec-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="780ec-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-155">PresenceunownedFieldUpgrade físico diferida</span><span class="sxs-lookup"><span data-stu-id="780ec-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="780ec-156">La configuración de presencia física se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="780ec-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="780ec-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-158"><dt>14</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-159">Desactive, habilite y active el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="780ec-160">Esta operación no se puede revertir.</span><span class="sxs-lookup"><span data-stu-id="780ec-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-161"><dt>4,5</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="780ec-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="780ec-163">Establece la provisión de que debe estar físicamente en presencia para establecer el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="780ec-164">Esta operación se invierte en la operación 16.</span><span class="sxs-lookup"><span data-stu-id="780ec-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="780ec-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-166"><dt>dieciséi</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="780ec-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="780ec-168">Establece el aprovisionamiento que no es necesario tener físicamente en presencia para establecer el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="780ec-169">Esta operación se invierte en la operación 15.</span><span class="sxs-lookup"><span data-stu-id="780ec-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="780ec-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-171"><dt>18</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="780ec-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="780ec-173">Establece la provisión de que debe estar físicamente en presencia para borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="780ec-174">Esta operación se invierte en la operación 18.</span><span class="sxs-lookup"><span data-stu-id="780ec-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="780ec-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-176"><dt>18</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="780ec-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="780ec-178">Establece el aprovisionamiento que no es necesario tener físicamente en presencia para borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="780ec-179">Esta operación se invierte en la operación 17.</span><span class="sxs-lookup"><span data-stu-id="780ec-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="780ec-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-181"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="780ec-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="780ec-183">Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="780ec-184">Esta operación se invierte en la operación 20.</span><span class="sxs-lookup"><span data-stu-id="780ec-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="780ec-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="780ec-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="780ec-188">Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="780ec-189">Esta operación se invierte en la operación 19.</span><span class="sxs-lookup"><span data-stu-id="780ec-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="780ec-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="780ec-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-192">Habilitar + Activar + borrar</span><span class="sxs-lookup"><span data-stu-id="780ec-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="780ec-193">Habilite, Active y desactive el TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="780ec-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="780ec-195"><dt>56</dt> </span><span class="sxs-lookup"><span data-stu-id="780ec-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="780ec-196">Habilitar + Activar + desactivar + habilitar + activar</span><span class="sxs-lookup"><span data-stu-id="780ec-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="780ec-197">Habilite, Active y desactive el TPM y, a continuación, habilite y vuelva a activar TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="780ec-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="780ec-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="780ec-199">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="780ec-199">Return value</span></span>

<span data-ttu-id="780ec-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="780ec-200">Type: **uint32**</span></span>

<span data-ttu-id="780ec-201">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="780ec-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="780ec-202">En la tabla siguiente se enumeran los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="780ec-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="780ec-203">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="780ec-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="780ec-204">Descripción</span><span class="sxs-lookup"><span data-stu-id="780ec-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="780ec-205"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="780ec-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="780ec-206">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="780ec-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="780ec-207"><dt>**TPM \_ E \_ PPI \_ ACPI \_ error**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="780ec-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="780ec-208">Error de hardware.</span><span class="sxs-lookup"><span data-stu-id="780ec-208">A hardware failure occurred.</span></span> <span data-ttu-id="780ec-209">Consulte al fabricante del equipo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="780ec-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="780ec-210">Observaciones</span><span class="sxs-lookup"><span data-stu-id="780ec-210">Remarks</span></span>

<span data-ttu-id="780ec-211">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="780ec-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="780ec-212">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="780ec-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="780ec-213">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="780ec-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="780ec-214">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="780ec-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="780ec-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="780ec-215">Requirements</span></span>



| <span data-ttu-id="780ec-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="780ec-216">Requirement</span></span> | <span data-ttu-id="780ec-217">Value</span><span class="sxs-lookup"><span data-stu-id="780ec-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="780ec-218">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="780ec-218">Minimum supported client</span></span><br/> | <span data-ttu-id="780ec-219">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="780ec-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="780ec-220">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="780ec-220">Minimum supported server</span></span><br/> | <span data-ttu-id="780ec-221">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="780ec-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="780ec-222">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="780ec-222">Namespace</span></span><br/>                | <span data-ttu-id="780ec-223">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="780ec-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="780ec-224">MOF</span><span class="sxs-lookup"><span data-stu-id="780ec-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="780ec-225"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="780ec-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="780ec-226">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="780ec-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="780ec-227"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="780ec-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="780ec-228">Vea también</span><span class="sxs-lookup"><span data-stu-id="780ec-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="780ec-229">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="780ec-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="780ec-230">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="780ec-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="780ec-231">**Disable**</span><span class="sxs-lookup"><span data-stu-id="780ec-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="780ec-232">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="780ec-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="780ec-233">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="780ec-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="780ec-234">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="780ec-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
