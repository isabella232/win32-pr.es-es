---
title: Método DeleteSBDbConnectionString de la clase Win32_SessionBrokerServiceProperties
description: Elimina las cadenas de conexión de base de datos (principal o secundaria) del registro.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- Método DeleteSBDbConnectionString Servicios de Escritorio remoto
- Método DeleteSBDbConnectionString Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método DeleteSBDbConnectionString
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676749"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="e565f-106">Método DeleteSBDbConnectionString de la \_ clase SessionBrokerServiceProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="e565f-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="e565f-107">Elimina las cadenas de conexión de base de datos (principal o secundaria) del registro.</span><span class="sxs-lookup"><span data-stu-id="e565f-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="e565f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e565f-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="e565f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e565f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e565f-110">*IsSecondaryConnString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e565f-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e565f-111">Si es **true**, se quita la cadena de conexión secundaria.</span><span class="sxs-lookup"><span data-stu-id="e565f-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="e565f-112">Si es **false**, se quita la cadena de conexión principal.</span><span class="sxs-lookup"><span data-stu-id="e565f-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e565f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e565f-113">Requirements</span></span>



| <span data-ttu-id="e565f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e565f-114">Requirement</span></span> | <span data-ttu-id="e565f-115">Value</span><span class="sxs-lookup"><span data-stu-id="e565f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e565f-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e565f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e565f-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e565f-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e565f-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e565f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e565f-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e565f-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="e565f-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e565f-120">Namespace</span></span><br/>                | <span data-ttu-id="e565f-121">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e565f-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="e565f-122">MOF</span><span class="sxs-lookup"><span data-stu-id="e565f-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e565f-123"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e565f-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e565f-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e565f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e565f-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e565f-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e565f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e565f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e565f-127">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="e565f-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





