---
title: Método SetMaxConnections de la clase Win32_TSGatewayServerSettings
description: Establece las propiedades MaxConnections y UnlimitedConnections, que controlan el número máximo de conexiones permitidas en el servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: cfdbacb7-4969-4ec5-8301-e8020f3af0cd
ms.tgt_platform: multiple
keywords:
- Método SetMaxConnections Servicios de Escritorio remoto
- Método SetMaxConnections Servicios de Escritorio remoto, clase Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings de clase Servicios de Escritorio remoto, método SetMaxConnections
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetMaxConnections
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e8a2fa18491232a058913fd338bb871b0a98aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676843"
---
# <a name="setmaxconnections-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="68162-106">Método SetMaxConnections de la \_ clase TSGatewayServerSettings de Win32</span><span class="sxs-lookup"><span data-stu-id="68162-106">SetMaxConnections method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="68162-107">Establece las propiedades **MaxConnections** y **UnlimitedConnections** , que controlan el número máximo de conexiones permitidas en el servidor de puerta de enlace de escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="68162-107">Sets the **MaxConnections** and **UnlimitedConnections** properties, which control the maximum number of allowed connections to the Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="68162-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68162-108">Syntax</span></span>


```mof
uint32 SetMaxConnections(
  [in] uint32  Connections,
  [in] boolean IsUnlimited
);
```



## <a name="parameters"></a><span data-ttu-id="68162-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="68162-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68162-110">*Conexiones* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="68162-110">*Connections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68162-111">Número de conexiones que este servidor debe aceptar.</span><span class="sxs-lookup"><span data-stu-id="68162-111">Number of connections that this server should accept.</span></span> <span data-ttu-id="68162-112">Para un número ilimitado de conexiones, establezca el parámetro *IsUnlimited* en **true**.</span><span class="sxs-lookup"><span data-stu-id="68162-112">For an unlimited number of connections, set the *IsUnlimited* parameter to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="68162-113">*IsUnlimited* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="68162-113">*IsUnlimited* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68162-114">Si **es true**, las conexiones al servicio no se limitan a un número específico.</span><span class="sxs-lookup"><span data-stu-id="68162-114">If **True**, connections to the service are not limited to a specific number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68162-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="68162-115">Return value</span></span>

<span data-ttu-id="68162-116">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="68162-116">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="68162-117">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="68162-117">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="68162-118">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="68162-118">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="68162-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68162-119">Remarks</span></span>

<span data-ttu-id="68162-120">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="68162-120">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="68162-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="68162-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="68162-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="68162-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="68162-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="68162-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="68162-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="68162-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="68162-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68162-125">Requirements</span></span>



| <span data-ttu-id="68162-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="68162-126">Requirement</span></span> | <span data-ttu-id="68162-127">Value</span><span class="sxs-lookup"><span data-stu-id="68162-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68162-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68162-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68162-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="68162-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="68162-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68162-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68162-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68162-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="68162-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68162-132">Namespace</span></span><br/>                | <span data-ttu-id="68162-133">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="68162-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="68162-134">MOF</span><span class="sxs-lookup"><span data-stu-id="68162-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68162-135"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68162-135"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="68162-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68162-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68162-137"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68162-137"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="68162-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="68162-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68162-139">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="68162-139">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

