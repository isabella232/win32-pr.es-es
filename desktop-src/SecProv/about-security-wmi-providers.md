---
description: Permita que las aplicaciones interactúen con el Módulo de plataforma segura (TPM) y el Cifrado de unidad BitLocker (BDE) mediante el marco de administración unificada de Instrumental de administración de Windows (WMI).
ms.assetid: acd1bc8e-3311-47f9-88b1-739f224e40e9
title: Acerca de los proveedores de WMI de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed75cebf14ee3eb419578111b7de15608661d91e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002585"
---
# <a name="about-security-wmi-providers"></a><span data-ttu-id="d6aa5-103">Acerca de los proveedores de WMI de seguridad</span><span class="sxs-lookup"><span data-stu-id="d6aa5-103">About Security WMI Providers</span></span>

<span data-ttu-id="d6aa5-104">Los proveedores de WMI de seguridad permiten a las aplicaciones interactuar con el Módulo de plataforma segura (TPM) y el Cifrado de unidad BitLocker (BDE) a través del marco de administración unificada de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6aa5-104">The Security WMI Providers allow applications to interact with the Trusted Platform Module (TPM) and BitLocker Drive Encryption (BDE) through the unified management framework of Windows Management Instrumentation (WMI).</span></span>



| <span data-ttu-id="d6aa5-105">Sección</span><span class="sxs-lookup"><span data-stu-id="d6aa5-105">Section</span></span>                                                                  | <span data-ttu-id="d6aa5-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6aa5-106">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6aa5-107">Referencia de proveedores de WMI de seguridad</span><span class="sxs-lookup"><span data-stu-id="d6aa5-107">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md) | <span data-ttu-id="d6aa5-108">Documentación de la API para las clases [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) y [**Win32 \_ TPM**](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d6aa5-108">API documentation for [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md) classes.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d6aa5-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6aa5-109">Remarks</span></span>

<span data-ttu-id="d6aa5-110">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d6aa5-110">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d6aa5-111">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="d6aa5-111">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d6aa5-112">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="d6aa5-112">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d6aa5-113">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d6aa5-113">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

 

 
