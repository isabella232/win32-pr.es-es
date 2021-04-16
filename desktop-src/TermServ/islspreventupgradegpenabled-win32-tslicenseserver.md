---
title: Método IsLSPreventUpgradeGPEnabled de la clase Win32_TSLicenseServer
description: Recupera si \ 0034; evita la actualización de licencias \ 0034; la configuración de directiva de grupo está habilitada en el servidor de licencias de Escritorio remoto.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Método IsLSPreventUpgradeGPEnabled Servicios de Escritorio remoto
- Método IsLSPreventUpgradeGPEnabled Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676814"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="2f21b-106">Método IsLSPreventUpgradeGPEnabled de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="2f21b-106">IsLSPreventUpgradeGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="2f21b-107">Recupera si está habilitada la configuración de directiva de grupo "impedir actualización de licencia" en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2f21b-107">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f21b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f21b-108">Syntax</span></span>


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="2f21b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f21b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f21b-110">*Habilitado* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2f21b-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f21b-111">Valor booleano que indica si está habilitada la configuración de directiva "impedir actualización de licencia".</span><span class="sxs-lookup"><span data-stu-id="2f21b-111">Boolean value that indicates whether the "prevent license upgrade" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f21b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f21b-112">Return value</span></span>

<span data-ttu-id="2f21b-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="2f21b-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="2f21b-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2f21b-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="2f21b-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2f21b-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f21b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f21b-116">Remarks</span></span>

<span data-ttu-id="2f21b-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2f21b-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="2f21b-118">Si está habilitada la configuración de directiva "impedir actualización de licencia", el servidor de licencias solo emitirá una CAL de RDS temporal para el cliente si no está disponible una CAL de RDS adecuada para el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="2f21b-118">If the "prevent license upgrade" policy setting is enabled, the license server will only issue a temporary RDS CAL to the client if an appropriate RDS CAL for the Remote Desktop Session Host (RD Session Host) server is not available.</span></span>

<span data-ttu-id="2f21b-119">La configuración de Directiva se encuentra en el siguiente nodo del editor de directivas de grupo local:</span><span class="sxs-lookup"><span data-stu-id="2f21b-119">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="2f21b-120">Configuración del equipo \\ plantillas administrativas \\ componentes de Windows \\ Terminal Services licencias de \\ TS</span><span class="sxs-lookup"><span data-stu-id="2f21b-120">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="2f21b-121">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2f21b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2f21b-122">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2f21b-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2f21b-123">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2f21b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2f21b-124">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2f21b-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2f21b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f21b-125">Requirements</span></span>



| <span data-ttu-id="2f21b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f21b-126">Requirement</span></span> | <span data-ttu-id="2f21b-127">Value</span><span class="sxs-lookup"><span data-stu-id="2f21b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f21b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f21b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2f21b-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2f21b-129">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="2f21b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f21b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2f21b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f21b-131">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2f21b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2f21b-132">Namespace</span></span><br/>                | <span data-ttu-id="2f21b-133">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="2f21b-133">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="2f21b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2f21b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f21b-135"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f21b-135"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f21b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f21b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f21b-137"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f21b-137"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f21b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f21b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f21b-139">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="2f21b-139">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

