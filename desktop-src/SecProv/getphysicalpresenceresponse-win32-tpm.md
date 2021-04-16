---
description: Devuelve los resultados de una operación de presencia física de TPM realizada.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Método GetPhysicalPresenceResponse de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686647"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="561c1-103">Método GetPhysicalPresenceResponse de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="561c1-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="561c1-104">El método **GetPhysicalPresenceResponse** de la clase [**Win32 \_ TPM**](win32-tpm.md) devuelve los resultados de una operación de presencia física de TPM que se realizó.</span><span class="sxs-lookup"><span data-stu-id="561c1-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="561c1-105">Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.</span><span class="sxs-lookup"><span data-stu-id="561c1-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="561c1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="561c1-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="561c1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="561c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="561c1-108">*Solicitud* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="561c1-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="561c1-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="561c1-109">Type: **uint32**</span></span>

<span data-ttu-id="561c1-110">Valor entero que especifica la operación de presencia física del TPM que se ha realizado.</span><span class="sxs-lookup"><span data-stu-id="561c1-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="561c1-111">Value</span><span class="sxs-lookup"><span data-stu-id="561c1-111">Value</span></span></th>
<th><span data-ttu-id="561c1-112">Significado</span><span class="sxs-lookup"><span data-stu-id="561c1-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-113"><dt>0,1</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-114">Ninguna solicitud.</span><span class="sxs-lookup"><span data-stu-id="561c1-114">No request.</span></span><br/> <span data-ttu-id="561c1-115">No se realizó ninguna operación de presencia física.</span><span class="sxs-lookup"><span data-stu-id="561c1-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-117">Habilite el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-117">Enable the TPM.</span></span><br/> <span data-ttu-id="561c1-118">Esta operación se invierte en la operación 2.</span><span class="sxs-lookup"><span data-stu-id="561c1-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="561c1-119">Para obtener más información, consulte estos métodos relacionados que no implican la presencia física:</span><span class="sxs-lookup"><span data-stu-id="561c1-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="561c1-120"><a href="enable-win32-tpm.md"><strong>Habilitar</strong></a></span><span class="sxs-lookup"><span data-stu-id="561c1-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="561c1-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="561c1-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-123">Deshabilite TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-123">Disable the TPM.</span></span><br/> <span data-ttu-id="561c1-124">Esta operación se invierte en la operación 1.</span><span class="sxs-lookup"><span data-stu-id="561c1-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="561c1-125">Para obtener más información, vea este método relacionado que no implica la presencia física: <a href="disable-win32-tpm.md"><strong>deshabilitar</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="561c1-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-126"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-127">Active el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-127">Activate the TPM.</span></span><br/> <span data-ttu-id="561c1-128">Esta operación se invierte en la operación 4.</span><span class="sxs-lookup"><span data-stu-id="561c1-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-130">Desactive el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="561c1-131">Esta operación se invierte en la operación 3.</span><span class="sxs-lookup"><span data-stu-id="561c1-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-132"><dt>5</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-133">Borre el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-133">Clear the TPM.</span></span><br/> <span data-ttu-id="561c1-134">Esta operación no se puede revertir.</span><span class="sxs-lookup"><span data-stu-id="561c1-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="561c1-135">Para obtener más información, consulte este método relacionado que no implica la presencia física: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="561c1-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-136"><dt>1,8</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-137">Habilitar y activar el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="561c1-138">Esta operación se invierte en la operación 7.</span><span class="sxs-lookup"><span data-stu-id="561c1-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-140">Desactivar y deshabilitar TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="561c1-141">Esta operación se invierte en la operación 6.</span><span class="sxs-lookup"><span data-stu-id="561c1-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-142"><dt>203</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-143">Permitir la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="561c1-144">Esta operación se invierte en la operación 9.</span><span class="sxs-lookup"><span data-stu-id="561c1-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-145"><dt>9</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-146">Impedir la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="561c1-147">Esta operación se invierte en la operación 8.</span><span class="sxs-lookup"><span data-stu-id="561c1-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-148"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-149">Habilitar, activar y permitir la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="561c1-150">Esta operación se invierte en la operación 11.</span><span class="sxs-lookup"><span data-stu-id="561c1-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-151"><dt>279</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-152">Desactive, deshabilite y evite la instalación de un propietario de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="561c1-153">Esta operación se invierte en la operación 10.</span><span class="sxs-lookup"><span data-stu-id="561c1-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="561c1-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-155">PresenceunownedFieldUpgrade físico diferida</span><span class="sxs-lookup"><span data-stu-id="561c1-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="561c1-156">La configuración de presencia física se ha actualizado.</span><span class="sxs-lookup"><span data-stu-id="561c1-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="561c1-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-158"><dt>14</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-159">Desactive, habilite y active el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="561c1-160">Esta operación no se puede revertir.</span><span class="sxs-lookup"><span data-stu-id="561c1-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-161"><dt>4,5</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="561c1-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="561c1-163">Establece la provisión de que debe estar físicamente en presencia para establecer el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="561c1-164">Esta operación se invierte en la operación 16.</span><span class="sxs-lookup"><span data-stu-id="561c1-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="561c1-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-166"><dt>dieciséi</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="561c1-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="561c1-168">Establece el aprovisionamiento que no es necesario tener físicamente en presencia para establecer el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="561c1-169">Esta operación se invierte en la operación 15.</span><span class="sxs-lookup"><span data-stu-id="561c1-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="561c1-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-171"><dt>18</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="561c1-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="561c1-173">Establece la provisión de que debe estar físicamente en presencia para borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="561c1-174">Esta operación se invierte en la operación 18.</span><span class="sxs-lookup"><span data-stu-id="561c1-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="561c1-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-176"><dt>18</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="561c1-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="561c1-178">Establece el aprovisionamiento que no es necesario tener físicamente en presencia para borrar el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="561c1-179">Esta operación se invierte en la operación 17.</span><span class="sxs-lookup"><span data-stu-id="561c1-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="561c1-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-181"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="561c1-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="561c1-183">Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="561c1-184">Esta operación se invierte en la operación 20.</span><span class="sxs-lookup"><span data-stu-id="561c1-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="561c1-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="561c1-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="561c1-188">Establece la provisión de que debe estar físicamente en presencia para mantener el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="561c1-189">Esta operación se invierte en la operación 19.</span><span class="sxs-lookup"><span data-stu-id="561c1-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="561c1-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="561c1-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-192">Habilitar + Activar + borrar</span><span class="sxs-lookup"><span data-stu-id="561c1-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="561c1-193">Habilite, Active y desactive el TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="561c1-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="561c1-195"><dt>56</dt> </span><span class="sxs-lookup"><span data-stu-id="561c1-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="561c1-196">Habilitar + Activar + desactivar + habilitar + activar</span><span class="sxs-lookup"><span data-stu-id="561c1-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="561c1-197">Habilite, Active y desactive el TPM y, a continuación, habilite y vuelva a activar TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="561c1-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista y Windows server 2008:</strong> Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="561c1-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="561c1-199">*Respuesta* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="561c1-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="561c1-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="561c1-200">Type: **uint32**</span></span>

<span data-ttu-id="561c1-201">Valor entero que especifica el resultado de realizar la operación de presencia física del TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="561c1-202">Una operación de presencia física se realiza correctamente si un usuario presente físicamente confirma la operación y si la operación se ejecuta sin errores.</span><span class="sxs-lookup"><span data-stu-id="561c1-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="561c1-203">Este valor puede contener cualquier error de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-203">This value may contain any TPM error.</span></span> <span data-ttu-id="561c1-204">En la tabla siguiente se enumeran algunas de las respuestas de error comunes.</span><span class="sxs-lookup"><span data-stu-id="561c1-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="561c1-205">Value</span><span class="sxs-lookup"><span data-stu-id="561c1-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="561c1-206">Significado</span><span class="sxs-lookup"><span data-stu-id="561c1-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="561c1-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="561c1-208">La operación del TPM solicitada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="561c1-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="561c1-209"><dt>**TPM \_ E \_ PPI \_ USER \_ Abort**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="561c1-210">El usuario rechazó la operación de TPM solicitada.</span><span class="sxs-lookup"><span data-stu-id="561c1-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="561c1-211"><dt>**TPM \_ E \_ PPP \_ BIOS \_ error**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="561c1-212">Error de BIOS al ejecutar la operación de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="561c1-213">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="561c1-213">Return value</span></span>

<span data-ttu-id="561c1-214">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="561c1-214">Type: **uint32**</span></span>

<span data-ttu-id="561c1-215">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="561c1-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="561c1-216">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="561c1-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="561c1-217">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="561c1-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="561c1-218">Descripción</span><span class="sxs-lookup"><span data-stu-id="561c1-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="561c1-219"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="561c1-220">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="561c1-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="561c1-221"><dt>**TPM \_ E \_ PPI \_ ACPI \_ error**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="561c1-222">Error de hardware.</span><span class="sxs-lookup"><span data-stu-id="561c1-222">A hardware failure occurred.</span></span> <span data-ttu-id="561c1-223">Consulte al fabricante del equipo para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="561c1-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="561c1-224">Observaciones</span><span class="sxs-lookup"><span data-stu-id="561c1-224">Remarks</span></span>

<span data-ttu-id="561c1-225">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="561c1-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="561c1-226">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="561c1-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="561c1-227">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="561c1-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="561c1-228">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="561c1-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="561c1-229">Requisitos</span><span class="sxs-lookup"><span data-stu-id="561c1-229">Requirements</span></span>



| <span data-ttu-id="561c1-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="561c1-230">Requirement</span></span> | <span data-ttu-id="561c1-231">Value</span><span class="sxs-lookup"><span data-stu-id="561c1-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="561c1-232">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="561c1-232">Minimum supported client</span></span><br/> | <span data-ttu-id="561c1-233">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="561c1-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="561c1-234">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="561c1-234">Minimum supported server</span></span><br/> | <span data-ttu-id="561c1-235">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="561c1-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="561c1-236">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="561c1-236">Namespace</span></span><br/>                | <span data-ttu-id="561c1-237">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="561c1-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="561c1-238">MOF</span><span class="sxs-lookup"><span data-stu-id="561c1-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="561c1-239"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="561c1-240">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="561c1-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="561c1-241"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="561c1-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="561c1-242">Vea también</span><span class="sxs-lookup"><span data-stu-id="561c1-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="561c1-243">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="561c1-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="561c1-244">**Claridad**</span><span class="sxs-lookup"><span data-stu-id="561c1-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="561c1-245">**Disable**</span><span class="sxs-lookup"><span data-stu-id="561c1-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="561c1-246">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="561c1-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="561c1-247">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="561c1-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
