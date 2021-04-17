---
title: Método SetSBDbConnectionStrings de la clase Win32_SessionBrokerServiceProperties
description: Guarda las cadenas de conexión de base de datos, tanto las principales como las secundarias, en el registro.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- Método SetSBDbConnectionStrings Servicios de Escritorio remoto
- Método SetSBDbConnectionStrings Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método SetSBDbConnectionStrings
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490577"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="3f393-106">Método SetSBDbConnectionStrings de la \_ clase SessionBrokerServiceProperties de Win32</span><span class="sxs-lookup"><span data-stu-id="3f393-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="3f393-107">Guarda las cadenas de conexión de base de datos, tanto las principales como las secundarias, en el registro.</span><span class="sxs-lookup"><span data-stu-id="3f393-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f393-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f393-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="3f393-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f393-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f393-110">*connStringToCentralDBRdcms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f393-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f393-111">Cadena de conexión principal.</span><span class="sxs-lookup"><span data-stu-id="3f393-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="3f393-112">*secondaryConnStringToCentralDBRdcms* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f393-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f393-113">La cadena de conexión secundaria.</span><span class="sxs-lookup"><span data-stu-id="3f393-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f393-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f393-114">Requirements</span></span>



| <span data-ttu-id="3f393-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f393-115">Requirement</span></span> | <span data-ttu-id="3f393-116">Value</span><span class="sxs-lookup"><span data-stu-id="3f393-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f393-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f393-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3f393-118">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3f393-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3f393-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f393-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3f393-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3f393-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="3f393-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f393-121">Namespace</span></span><br/>                | <span data-ttu-id="3f393-122">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3f393-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="3f393-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3f393-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f393-124"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f393-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f393-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f393-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f393-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f393-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3f393-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f393-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f393-128">**Win32 \_ SessionBrokerServiceProperties**</span><span class="sxs-lookup"><span data-stu-id="3f393-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





