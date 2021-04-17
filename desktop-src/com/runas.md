---
title: RunAs
description: Configura una clase para que se ejecute en una cuenta de usuario específica cuando está activada por un cliente remoto sin escribirse como una aplicación de servicio.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valor del registro runas COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705033"
---
# <a name="runas"></a><span data-ttu-id="29ef8-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="29ef8-104">RunAs</span></span>

<span data-ttu-id="29ef8-105">Configura una clase para que se ejecute en una cuenta de usuario específica cuando está activada por un cliente remoto sin escribirse como una aplicación de servicio.</span><span class="sxs-lookup"><span data-stu-id="29ef8-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="29ef8-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="29ef8-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="29ef8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29ef8-107">Remarks</span></span>

<span data-ttu-id="29ef8-108">El valor especifica el nombre de usuario y debe tener el formato *nombreDeUsuario*, *dominio ***\\*** nombreDeUsuario* o la cadena "usuario interactivo".</span><span class="sxs-lookup"><span data-stu-id="29ef8-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="29ef8-109">También puede especificar las cadenas "NT Authority \\ LocalService" (para el servicio local) y "NT Authority \\ NetworkService" (para el servicio de red).</span><span class="sxs-lookup"><span data-stu-id="29ef8-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="29ef8-110">También puede especificar la cadena "NT Authority \\ System" cuando {*AppID \_ GUID*} hace referencia a un servidor com que ya se ha iniciado o que tiene una entrada en la tabla de clases.</span><span class="sxs-lookup"><span data-stu-id="29ef8-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="29ef8-111">Sin embargo, no puede usar "NT Authority \\ System" con un servidor com que no se haya iniciado todavía.</span><span class="sxs-lookup"><span data-stu-id="29ef8-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="29ef8-112">La contraseña predeterminada para ' NT Authority \\ LocalService ', ' NT Authority \\ NetworkService ' y ' NT Authority \\ System ' es ' ' (cadena vacía).</span><span class="sxs-lookup"><span data-stu-id="29ef8-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="29ef8-113">A partir de Windows Vista, ya no se necesita una contraseña vacía para configurar las opciones de ejecución de "NT Authority \\ LocalService", "NT Authority \\ NetworkService" y "NT Authority \\ System". </span><span class="sxs-lookup"><span data-stu-id="29ef8-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="29ef8-114">Es posible que las clases configuradas para ejecutarse como un usuario determinado no se registren en ninguna otra identidad, por lo que se producirá un error en las llamadas a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con este CLSID a menos que com haya iniciado el proceso en nombre de una solicitud de activación real.</span><span class="sxs-lookup"><span data-stu-id="29ef8-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="29ef8-115">El nombre de usuario se toma del valor **runas** de la clave **AppID** de la clase.</span><span class="sxs-lookup"><span data-stu-id="29ef8-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="29ef8-116">Si el nombre de usuario es "usuario interactivo", el servidor se ejecuta en la identidad del usuario que ha iniciado sesión actualmente y está conectado al escritorio interactivo.</span><span class="sxs-lookup"><span data-stu-id="29ef8-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="29ef8-117">De lo contrario, la contraseña se recupera de una parte del registro que solo está disponible para los administradores del equipo y del sistema.</span><span class="sxs-lookup"><span data-stu-id="29ef8-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="29ef8-118">El nombre de usuario y la contraseña se usan para crear una sesión de inicio de sesión en la que se ejecuta el servidor.</span><span class="sxs-lookup"><span data-stu-id="29ef8-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="29ef8-119">Cuando se inicia de esta manera, el usuario se ejecuta con su propio escritorio y estación de ventana, y no comparte los identificadores de ventana, el portapapeles u otros elementos de la interfaz de usuario con el usuario interactivo u otro usuario que se ejecute en otras cuentas de usuario.</span><span class="sxs-lookup"><span data-stu-id="29ef8-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="29ef8-120">Para establecer una contraseña para una clase **runas** , debe usar la herramienta administrativa DCOMCNFG instalada en el directorio del sistema.</span><span class="sxs-lookup"><span data-stu-id="29ef8-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="29ef8-121">Para las identidades de **runas** utilizadas por los servidores DCOM, la cuenta de usuario especificada en el valor debe tener derechos para iniciar sesión como un trabajo por lotes.</span><span class="sxs-lookup"><span data-stu-id="29ef8-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="29ef8-122">Este derecho se puede agregar mediante la herramienta administrativa de la Directiva de seguridad local.</span><span class="sxs-lookup"><span data-stu-id="29ef8-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="29ef8-123">Vaya a **Directivas locales** y Abra **asignación de derechos de usuario**.</span><span class="sxs-lookup"><span data-stu-id="29ef8-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="29ef8-124">Seleccione **iniciar sesión como trabajo por lotes** y agregue la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="29ef8-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="29ef8-125">El valor **runas** no se utiliza para los servidores configurados para ejecutarse como servicios.</span><span class="sxs-lookup"><span data-stu-id="29ef8-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="29ef8-126">Los servicios COM que deben ejecutarse con una identidad distinta de LocalSystem deben establecer el nombre de usuario y la contraseña adecuados mediante el applet del panel de control de servicios o las funciones del controlador de servicio.</span><span class="sxs-lookup"><span data-stu-id="29ef8-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="29ef8-127">(Para obtener más información acerca de estas funciones, consulte [servicios](/windows/desktop/Services/services)).</span><span class="sxs-lookup"><span data-stu-id="29ef8-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="29ef8-128">A partir de Microsoft Windows Server 2003, la clase AppID se lee explícitamente desde **\_ \_ las clases de software de máquina local HKEY \\ \\ \\ AppID**, que, a diferencia de la mayoría de las claves del registro, no es intercambiable con **HKEY \_ classes \_ raíz \\ AppID**.</span><span class="sxs-lookup"><span data-stu-id="29ef8-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="29ef8-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29ef8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29ef8-130">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="29ef8-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 