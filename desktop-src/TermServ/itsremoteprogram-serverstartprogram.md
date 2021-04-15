---
title: ITSRemoteProgram ServerStartProgram, método
description: Especifica un programa RemoteApp para iniciarse en la sesión remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Método ServerStartProgram Servicios de Escritorio remoto
- Método ServerStartProgram Servicios de Escritorio remoto, interfaz ITSRemoteProgram
- Interfaz ITSRemoteProgram Servicios de Escritorio remoto, método ServerStartProgram
- Método ServerStartProgram Servicios de Escritorio remoto, interfaz ITSRemoteProgram2
- Interfaz ITSRemoteProgram2 Servicios de Escritorio remoto, método ServerStartProgram
- Método ServerStartProgram Servicios de Escritorio remoto, interfaz ITSRemoteProgram3
- Interfaz ITSRemoteProgram3 Servicios de Escritorio remoto, método ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534431"
---
# <a name="itsremoteprogramserverstartprogram-method"></a><span data-ttu-id="4ec61-110">ITSRemoteProgram:: ServerStartProgram (método)</span><span class="sxs-lookup"><span data-stu-id="4ec61-110">ITSRemoteProgram::ServerStartProgram method</span></span>

<span data-ttu-id="4ec61-111">Especifica un programa RemoteApp para iniciarse en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="4ec61-111">Specifies a RemoteApp program to start in the remote session.</span></span> <span data-ttu-id="4ec61-112">Esta función se debe invocar en una sesión conectada (después de que se reciba la notificación conectada a la sesión en el cliente).</span><span class="sxs-lookup"><span data-stu-id="4ec61-112">This function must be invoked on a connected session (after the session connected notification is received at the client).</span></span> <span data-ttu-id="4ec61-113">Se puede iniciar cualquier número de Programas RemoteApp en una sesión.</span><span class="sxs-lookup"><span data-stu-id="4ec61-113">Any number of RemoteApp programs can be started in a session.</span></span> <span data-ttu-id="4ec61-114">Se agotará el tiempo de espera de una sesión de RemoteApp si no se inicia ningún programa RemoteApp en la sesión en el límite de tiempo de espera, que es de dos minutos para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4ec61-114">A RemoteApp session will time out if no RemoteApp program is started in the session within the time-out limit, which is two minutes for Windows Server 2008.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ec61-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ec61-115">Syntax</span></span>


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a><span data-ttu-id="4ec61-116">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ec61-116">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ec61-117">*bstrExecutablePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ec61-117">*bstrExecutablePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec61-118">La ruta de acceso del archivo ejecutable del programa RemoteApp en el servidor.</span><span class="sxs-lookup"><span data-stu-id="4ec61-118">The path of the RemoteApp program executable file on the server.</span></span>

</dd> <dt>

<span data-ttu-id="4ec61-119">*bstrFilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ec61-119">*bstrFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec61-120">La ruta de acceso de un archivo que se va a abrir en el servidor a través de una asociación de archivo, por ejemplo "C: \\ \\ documents \\ \\MyReport.docx".</span><span class="sxs-lookup"><span data-stu-id="4ec61-120">The path of a file to open on the server through a file association, for example "C:\\\\Documents\\\\MyReport.docx".</span></span> <span data-ttu-id="4ec61-121">Si especifica *bstrFilePath*, no debe especificar el parámetro *bstrExecutablePath* y viceversa.</span><span class="sxs-lookup"><span data-stu-id="4ec61-121">If you specify *bstrFilePath*, you should not specify the *bstrExecutablePath* parameter, and vice versa.</span></span> <span data-ttu-id="4ec61-122">Solo debe especificar uno de los parámetros.</span><span class="sxs-lookup"><span data-stu-id="4ec61-122">You should only specify one of the parameters.</span></span>

</dd> <dt>

<span data-ttu-id="4ec61-123">*bstrWorkingDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ec61-123">*bstrWorkingDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec61-124">El directorio de trabajo en el servidor para el programa RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="4ec61-124">The working directory on the server for the RemoteApp program.</span></span>

</dd> <dt>

<span data-ttu-id="4ec61-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ec61-125">*vbExpandEnvVarInWorkingDirectoryOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec61-126">Indica si el servidor debe expandir las variables de entorno en la ruta de acceso del directorio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="4ec61-126">Indicates whether the server should expand environment variables in the working directory path.</span></span> <span data-ttu-id="4ec61-127">Establezca este parámetro en **Variant \_ true** si la ruta de acceso del directorio de trabajo contiene variables de entorno o **Variant \_ false** si la ruta de acceso del directorio de trabajo no contiene variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="4ec61-127">Set this parameter to **VARIANT\_TRUE** if the working directory path contains environment variables, or **VARIANT\_FALSE** if the working directory path does not contain environment variables.</span></span>

</dd> <dt>

<span data-ttu-id="4ec61-128">*bstrArguments* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ec61-128">*bstrArguments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec61-129">Argumentos de la línea de comandos para el programa RemoteApp que se especifican en *bstrExecutablePath*.</span><span class="sxs-lookup"><span data-stu-id="4ec61-129">The command-line arguments for the RemoteApp program that are specified in *bstrExecutablePath*.</span></span> <span data-ttu-id="4ec61-130">Establézcalo en **null** si no se especifica *bstrExecutablePath* .</span><span class="sxs-lookup"><span data-stu-id="4ec61-130">Set this to **NULL** if *bstrExecutablePath* is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="4ec61-131">*vbExpandEnvVarInArgumentsOnServer* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4ec61-131">*vbExpandEnvVarInArgumentsOnServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ec61-132">Indica si el servidor debe expandir las variables de entorno en los argumentos de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="4ec61-132">Indicates whether the server should expand environment variables in the command-line arguments.</span></span> <span data-ttu-id="4ec61-133">Establezca este parámetro en **Variant \_ true** si los argumentos contienen variables de entorno o **Variant \_ false** si los argumentos no contienen variables de entorno.</span><span class="sxs-lookup"><span data-stu-id="4ec61-133">Set this parameter to **VARIANT\_TRUE** if the arguments contain environment variables, or **VARIANT\_FALSE** if the arguments do not contain environment variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ec61-134">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ec61-134">Return value</span></span>

<span data-ttu-id="4ec61-135">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4ec61-135">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ec61-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ec61-136">Requirements</span></span>



| <span data-ttu-id="4ec61-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ec61-137">Requirement</span></span> | <span data-ttu-id="4ec61-138">Value</span><span class="sxs-lookup"><span data-stu-id="4ec61-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ec61-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ec61-139">Minimum supported client</span></span><br/> | <span data-ttu-id="4ec61-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ec61-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4ec61-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ec61-141">Minimum supported server</span></span><br/> | <span data-ttu-id="4ec61-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ec61-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4ec61-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ec61-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ec61-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec61-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ec61-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ec61-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ec61-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ec61-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ec61-147">IID</span><span class="sxs-lookup"><span data-stu-id="4ec61-147">IID</span></span><br/>                      | <span data-ttu-id="4ec61-148">IID \_ ITSRemoteProgram se define como FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="4ec61-148">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="4ec61-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ec61-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ec61-150">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="4ec61-150">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="4ec61-151">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="4ec61-151">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="4ec61-152">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="4ec61-152">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





