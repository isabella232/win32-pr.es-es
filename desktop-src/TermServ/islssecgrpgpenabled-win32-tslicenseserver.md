---
title: Método IsLSSecGrpGPEnabled de la clase Win32_TSLicenseServer
description: Recupera si el grupo de seguridad del servidor de licencias \ 0034; \ 0034; la configuración de directiva de grupo está habilitada en el servidor de licencias de Escritorio remoto.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Método IsLSSecGrpGPEnabled Servicios de Escritorio remoto
- Método IsLSSecGrpGPEnabled Servicios de Escritorio remoto, clase Win32_TSLicenseServer
- Win32_TSLicenseServer de clase Servicios de Escritorio remoto, método IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150493"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="fb809-106">Método IsLSSecGrpGPEnabled de la \_ clase TSLicenseServer de Win32</span><span class="sxs-lookup"><span data-stu-id="fb809-106">IsLSSecGrpGPEnabled method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="fb809-107">Recupera si el valor de directiva de grupo "grupo de seguridad del servidor de licencias" está habilitado en el servidor de licencias de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="fb809-107">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb809-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb809-108">Syntax</span></span>


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="fb809-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb809-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb809-110">*Habilitado* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fb809-110">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb809-111">Valor booleano que indica si está habilitada la configuración de directiva "grupo de seguridad del servidor de licencias".</span><span class="sxs-lookup"><span data-stu-id="fb809-111">Boolean value that indicates whether the "license server security group" policy setting is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb809-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb809-112">Return value</span></span>

<span data-ttu-id="fb809-113">Si el método se ejecuta correctamente, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="fb809-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="fb809-114">Si el método no se realiza correctamente, devuelve un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="fb809-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="fb809-115">Para obtener una lista de códigos de error, vea [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fb809-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb809-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb809-116">Remarks</span></span>

<span data-ttu-id="fb809-117">Para llamar a este método, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="fb809-117">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="fb809-118">La configuración de directiva "grupo de seguridad del servidor de licencias" le permite especificar los servidores host de sesión de Escritorio remoto (host de sesión de escritorio remoto) que pueden ponerse en contacto con el servidor de licencias para obtener Servicios de Escritorio remoto licencias de acceso de cliente (cal de RDS).</span><span class="sxs-lookup"><span data-stu-id="fb809-118">The "license server security group" policy setting allows you to specify the Remote Desktop Session Host (RD Session Host) servers that are permitted to contact the license server to obtain Remote Desktop Services client access licenses (RDS CALs).</span></span> <span data-ttu-id="fb809-119">Si la configuración de directiva está habilitada en el servidor de licencias, el servidor solo responderá a las solicitudes CAL de RDS de los servidores host de sesión de escritorio remoto cuyas cuentas de equipo sean miembros del grupo local de Terminal Server equipos en el servidor de licencias.</span><span class="sxs-lookup"><span data-stu-id="fb809-119">If the policy setting is enabled on the license server, the server will only respond to RDS CAL requests from RD Session Host servers whose computer accounts are members of the Terminal Server Computers local group on the license server.</span></span>

<span data-ttu-id="fb809-120">La configuración de Directiva se encuentra en el siguiente nodo del editor de directivas de grupo local:</span><span class="sxs-lookup"><span data-stu-id="fb809-120">The policy setting is located in the following node of the local group policy editor:</span></span>

<span data-ttu-id="fb809-121">Configuración del equipo \\ plantillas administrativas \\ componentes de Windows \\ Terminal Services licencias de \\ TS</span><span class="sxs-lookup"><span data-stu-id="fb809-121">Computer Configuration\\Administrative Templates\\Windows Components\\Terminal Services\\TS Licensing</span></span>

<span data-ttu-id="fb809-122">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="fb809-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fb809-123">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fb809-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="fb809-124">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="fb809-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fb809-125">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="fb809-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="fb809-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb809-126">Requirements</span></span>



| <span data-ttu-id="fb809-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb809-127">Requirement</span></span> | <span data-ttu-id="fb809-128">Value</span><span class="sxs-lookup"><span data-stu-id="fb809-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb809-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb809-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fb809-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fb809-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="fb809-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fb809-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fb809-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb809-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="fb809-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fb809-133">Namespace</span></span><br/>                | <span data-ttu-id="fb809-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="fb809-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="fb809-135">MOF</span><span class="sxs-lookup"><span data-stu-id="fb809-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb809-136"><dt>TlsWmiProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb809-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb809-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb809-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb809-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb809-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb809-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="fb809-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb809-140">**Win32 \_ TSLicenseServer**</span><span class="sxs-lookup"><span data-stu-id="fb809-140">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

