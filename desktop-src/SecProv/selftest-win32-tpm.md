---
description: Realiza una prueba automática del TPM y devuelve el resultado.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Método SelfTest de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666382"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="cb367-103">Método SelfTest de la \_ clase Win32 TPM</span><span class="sxs-lookup"><span data-stu-id="cb367-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="cb367-104">El método **SelfTest** de la clase [**Win32 \_ TPM**](win32-tpm.md) realiza una prueba automática del TPM y devuelve el resultado.</span><span class="sxs-lookup"><span data-stu-id="cb367-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="cb367-105">Una prueba automática de TPM se ejecuta automáticamente cuando se inicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="cb367-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb367-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb367-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="cb367-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb367-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb367-108">*SelfTestResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb367-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb367-109">Tipo: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="cb367-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="cb367-110">Matriz de bytes que contiene el resultado de la prueba automática.</span><span class="sxs-lookup"><span data-stu-id="cb367-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="cb367-111">El formato de este parámetro es específico del fabricante.</span><span class="sxs-lookup"><span data-stu-id="cb367-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb367-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb367-112">Return value</span></span>

<span data-ttu-id="cb367-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cb367-113">Type: **uint32**</span></span>

<span data-ttu-id="cb367-114">Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.</span><span class="sxs-lookup"><span data-stu-id="cb367-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="cb367-115">En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.</span><span class="sxs-lookup"><span data-stu-id="cb367-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="cb367-116">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb367-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="cb367-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb367-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="cb367-118"><dt>**S \_ OK**</dt> <dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="cb367-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="cb367-119">El método se ejecutó correctamente.</span><span class="sxs-lookup"><span data-stu-id="cb367-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb367-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb367-120">Remarks</span></span>

<span data-ttu-id="cb367-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="cb367-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cb367-122">Los archivos MOF no se instalan como parte de la Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="cb367-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="cb367-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="cb367-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cb367-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="cb367-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb367-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb367-125">Requirements</span></span>



| <span data-ttu-id="cb367-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb367-126">Requirement</span></span> | <span data-ttu-id="cb367-127">Value</span><span class="sxs-lookup"><span data-stu-id="cb367-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb367-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb367-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cb367-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb367-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cb367-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb367-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cb367-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb367-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cb367-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb367-132">Namespace</span></span><br/>                | <span data-ttu-id="cb367-133">\\MicrosoftTpm de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="cb367-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="cb367-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cb367-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb367-135"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb367-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb367-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb367-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb367-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="cb367-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb367-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb367-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb367-139">**TPM de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="cb367-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
