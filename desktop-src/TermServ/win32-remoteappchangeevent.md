---
title: Win32_RemoteAppChangeEvent (clase)
description: Representa un cambio en la configuración de RemoteApp de Windows Server 2008 R2 en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 3434ee4e-283e-4147-a73b-c131e8af6c57
ms.tgt_platform: multiple
keywords:
- Win32_RemoteAppChangeEvent clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RemoteAppChangeEvent de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RemoteAppChangeEvent
- Win32_RemoteAppChangeEvent.SECURITY_DESCRIPTOR
- Win32_RemoteAppChangeEvent.TIME_CREATED
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5355d057038e97e9f381646134ff6487541f67f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150284"
---
# <a name="win32_remoteappchangeevent-class"></a><span data-ttu-id="c6f4b-105">\_Clase Win32 RemoteAppChangeEvent</span><span class="sxs-lookup"><span data-stu-id="c6f4b-105">Win32\_RemoteAppChangeEvent class</span></span>

<span data-ttu-id="c6f4b-106">Representa un cambio en la configuración de RemoteApp de Windows Server 2008 R2 en el servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-106">Represents a change to Windows Server 2008 R2 RemoteApp settings on the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f4b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c6f4b-107">Syntax</span></span>

``` syntax
class Win32_RemoteAppChangeEvent : ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c6f4b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c6f4b-108">Members</span></span>

<span data-ttu-id="c6f4b-109">La **clase \_ RemoteAppChangeEvent de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c6f4b-109">The **Win32\_RemoteAppChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c6f4b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6f4b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c6f4b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c6f4b-111">Properties</span></span>

<span data-ttu-id="c6f4b-112">La **clase \_ RemoteAppChangeEvent de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-112">The **Win32\_RemoteAppChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c6f4b-113">**descriptor de seguridad \_**</span><span class="sxs-lookup"><span data-stu-id="c6f4b-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f4b-114">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="c6f4b-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c6f4b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6f4b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f4b-116">Descriptor utilizado por el proveedor de eventos para determinar qué usuarios pueden recibir el evento.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c6f4b-117">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-117">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="c6f4b-118">Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-118">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="c6f4b-119">**HORA de \_ creación**</span><span class="sxs-lookup"><span data-stu-id="c6f4b-119">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c6f4b-120">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c6f4b-120">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c6f4b-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c6f4b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c6f4b-122">Valor único que indica la hora a la que se generó el evento.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-122">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="c6f4b-123">Se trata de un valor de 64 bits que representa el número de intervalos de 100 segundos después del 1 de enero de 1601.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-123">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c6f4b-124">La información está en el formato de hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-124">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="c6f4b-125">Esta propiedad se hereda del [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="c6f4b-126">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-126">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c6f4b-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c6f4b-127">Remarks</span></span>

<span data-ttu-id="c6f4b-128">Para conectarse al espacio de nombres "root \\ cimv2 \\ TerminalServices", el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-128">To connect to the "Root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="c6f4b-129">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="c6f4b-129">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="c6f4b-130">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-130">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="c6f4b-131">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-131">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="c6f4b-132">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c6f4b-133">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-133">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="c6f4b-134">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="c6f4b-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c6f4b-135">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="c6f4b-135">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f4b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6f4b-136">Requirements</span></span>



| <span data-ttu-id="c6f4b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f4b-137">Requirement</span></span> | <span data-ttu-id="c6f4b-138">Value</span><span class="sxs-lookup"><span data-stu-id="c6f4b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f4b-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6f4b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f4b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c6f4b-140">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c6f4b-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6f4b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f4b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c6f4b-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c6f4b-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c6f4b-143">Namespace</span></span><br/>                | <span data-ttu-id="c6f4b-144">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c6f4b-144">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c6f4b-145">MOF</span><span class="sxs-lookup"><span data-stu-id="c6f4b-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c6f4b-146"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c6f4b-146"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="c6f4b-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c6f4b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6f4b-148"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6f4b-148"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

