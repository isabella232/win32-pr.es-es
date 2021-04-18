---
description: Desasocia la imagen de almacenamiento montada que está asociada a esta clase.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Método DetachVirtualHardDisk de la clase Msvm_MountedStorageImage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0d411134d85fe70163b2e08eebed0ff0d4b88e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688069"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a><span data-ttu-id="d571f-103">Método DetachVirtualHardDisk de la \_ clase MountedStorageImage de MSVM</span><span class="sxs-lookup"><span data-stu-id="d571f-103">DetachVirtualHardDisk method of the Msvm\_MountedStorageImage class</span></span>

<span data-ttu-id="d571f-104">Desasocia la imagen de almacenamiento montada que está asociada a esta clase.</span><span class="sxs-lookup"><span data-stu-id="d571f-104">Detaches the mounted storage image that is associated with this class.</span></span>

## <a name="syntax"></a><span data-ttu-id="d571f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d571f-105">Syntax</span></span>


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a><span data-ttu-id="d571f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d571f-106">Parameters</span></span>

<span data-ttu-id="d571f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d571f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d571f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d571f-108">Return value</span></span>

<span data-ttu-id="d571f-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d571f-109">Type: **uint32**</span></span>

<span data-ttu-id="d571f-110">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d571f-110">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d571f-111">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="d571f-111">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d571f-112">**Error** (1)</span><span class="sxs-lookup"><span data-stu-id="d571f-112">**Failed** (1)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="d571f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d571f-113">Remarks</span></span>

<span data-ttu-id="d571f-114">El acceso a la clase [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="d571f-114">Access to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="d571f-115">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="d571f-115">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="d571f-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d571f-116">Examples</span></span>

<span data-ttu-id="d571f-117">En el siguiente ejemplo de C# se muestra cómo desasociar un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="d571f-117">The following C# example shows how to detach a virtual hard disk file.</span></span> <span data-ttu-id="d571f-118">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="d571f-118">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="d571f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d571f-119">Requirements</span></span>



| <span data-ttu-id="d571f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d571f-120">Requirement</span></span> | <span data-ttu-id="d571f-121">Value</span><span class="sxs-lookup"><span data-stu-id="d571f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d571f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d571f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d571f-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d571f-123">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d571f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d571f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d571f-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d571f-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d571f-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d571f-126">Namespace</span></span><br/>                | <span data-ttu-id="d571f-127">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d571f-127">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d571f-128">MOF</span><span class="sxs-lookup"><span data-stu-id="d571f-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d571f-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d571f-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d571f-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d571f-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d571f-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d571f-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d571f-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d571f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d571f-133">**MSVM \_ MountedStorageImage**</span><span class="sxs-lookup"><span data-stu-id="d571f-133">**Msvm\_MountedStorageImage**</span></span>](msvm-mountedstorageimage.md)
</dt> </dl>

 

