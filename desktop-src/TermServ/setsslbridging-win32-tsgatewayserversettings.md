---
title: Método SetSslBridging de la clase Win32_TSGatewayServerSettings
description: Establece el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 11885b8b-491e-4d90-b4d4-f0a0fbe68cb1
ms.tgt_platform: multiple
keywords:
- Método SetSslBridging Servicios de Escritorio remoto
- Método SetSslBridging Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetSslBridging
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetSslBridging
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77181fb8d8661ec7ea7dc0ce70532281fb9c1bde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422417"
---
# <a name="setsslbridging-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="2fd5d-106">Método SetSslBridging de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="2fd5d-106">SetSslBridging method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="2fd5d-107">Establece el tipo de protocolo de puente SSL que va a usar el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="2fd5d-107">Sets the type of SSL bridging to be used by the Remote Desktop Gateway (RD Gateway) server.</span></span> <span data-ttu-id="2fd5d-108">Este valor se almacena en la propiedad **SslBridging** .</span><span class="sxs-lookup"><span data-stu-id="2fd5d-108">This value is stored in the **SslBridging** property.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2fd5d-109">Cuando se cambia el tipo de protocolo de puente SSL con este método, el servicio de puerta de enlace de escritorio remoto debe reiniciarse para que este cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-109">When the SSL bridging type is changed with this method, the RD Gateway service must be restarted to make this change take effect.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2fd5d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fd5d-110">Syntax</span></span>


```mof
uint32 SetSslBridging(
  [in] uint32 SslBridging
);
```



## <a name="parameters"></a><span data-ttu-id="2fd5d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2fd5d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fd5d-112">*SslBridging* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2fd5d-112">*SslBridging* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fd5d-113">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fd5d-113">Type: **uint32**</span></span>

<span data-ttu-id="2fd5d-114">Especifica el nuevo valor de protocolo de puente SSL.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-114">Specifies the new SSL bridging value.</span></span> <span data-ttu-id="2fd5d-115">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-115">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="2fd5d-116">0</span><span class="sxs-lookup"><span data-stu-id="2fd5d-116">0</span></span>
</dt> <dd>

<span data-ttu-id="2fd5d-117">Sin puentes SSL.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-117">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="2fd5d-118">1</span><span class="sxs-lookup"><span data-stu-id="2fd5d-118">1</span></span>
</dt> <dd>

<span data-ttu-id="2fd5d-119">Puente de HTTPS a HTTP.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-119">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="2fd5d-120">2</span><span class="sxs-lookup"><span data-stu-id="2fd5d-120">2</span></span>
</dt> <dd>

<span data-ttu-id="2fd5d-121">Puente de HTTPS a HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-121">HTTPS to HTTPS bridging.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fd5d-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2fd5d-122">Return value</span></span>

<span data-ttu-id="2fd5d-123">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2fd5d-123">Type: **uint32**</span></span>

<span data-ttu-id="2fd5d-124">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-124">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2fd5d-125">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-125">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2fd5d-126">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2fd5d-126">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fd5d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2fd5d-127">Remarks</span></span>

<span data-ttu-id="2fd5d-128">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-128">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2fd5d-129">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2fd5d-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2fd5d-130">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-130">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2fd5d-131">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2fd5d-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2fd5d-132">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2fd5d-132">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fd5d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fd5d-133">Requirements</span></span>



| <span data-ttu-id="2fd5d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fd5d-134">Requirement</span></span> | <span data-ttu-id="2fd5d-135">Value</span><span class="sxs-lookup"><span data-stu-id="2fd5d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fd5d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fd5d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2fd5d-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2fd5d-137">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2fd5d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fd5d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2fd5d-139">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="2fd5d-139">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="2fd5d-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2fd5d-140">Namespace</span></span><br/>                | <span data-ttu-id="2fd5d-141">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2fd5d-141">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2fd5d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2fd5d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fd5d-143"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fd5d-143"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fd5d-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fd5d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fd5d-145"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fd5d-145"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2fd5d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2fd5d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fd5d-147">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="2fd5d-147">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

