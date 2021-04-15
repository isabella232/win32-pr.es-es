---
title: Moniker de elevación COM
description: El moniker de elevación de COM permite a las aplicaciones que se ejecutan en control de cuentas de usuario (UAC) activar las clases COM con privilegios elevados. Para obtener más información, consulte enfoque de privilegios mínimos.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104488382"
---
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="b2e75-104">Moniker de elevación COM</span><span class="sxs-lookup"><span data-stu-id="b2e75-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="b2e75-105">El moniker de elevación de COM permite a las aplicaciones que se ejecutan en control de cuentas de usuario (UAC) activar las clases COM con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="b2e75-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="b2e75-106">Para obtener más información, consulte [enfoque de privilegios mínimos](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="b2e75-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="b2e75-107">Cuándo utilizar el moniker de elevación</span><span class="sxs-lookup"><span data-stu-id="b2e75-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="b2e75-108">El moniker de elevación se utiliza para activar una clase COM con el fin de lograr una función específica y limitada que requiere privilegios elevados, como cambiar la fecha y la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="b2e75-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="b2e75-109">La elevación requiere la participación de una clase COM y su cliente.</span><span class="sxs-lookup"><span data-stu-id="b2e75-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="b2e75-110">La clase COM se debe configurar para admitir la elevación mediante la anotación de la entrada del registro, como se describe en la sección requisitos.</span><span class="sxs-lookup"><span data-stu-id="b2e75-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="b2e75-111">El cliente COM debe solicitar la elevación mediante el moniker de elevación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="b2e75-112">El moniker de elevación no está diseñado para proporcionar compatibilidad con aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b2e75-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="b2e75-113">Por ejemplo, si desea ejecutar una aplicación COM heredada como WinWord como servidor con privilegios elevados, debe configurar el ejecutable del cliente COM para que requiera elevación, en lugar de activar la clase de la aplicación heredada con el moniker de elevación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="b2e75-114">Cuando el cliente COM con privilegios elevados llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mediante el CLSID de la aplicación heredada, el estado elevado del cliente pasará al proceso del servidor.</span><span class="sxs-lookup"><span data-stu-id="b2e75-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="b2e75-115">No toda la funcionalidad de COM es compatible con la elevación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="b2e75-116">Entre las funciones que no funcionarán se incluyen:</span><span class="sxs-lookup"><span data-stu-id="b2e75-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="b2e75-117">La elevación no fluye desde un cliente a un servidor COM remoto.</span><span class="sxs-lookup"><span data-stu-id="b2e75-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="b2e75-118">Si un cliente activa un servidor COM remoto con el moniker de elevación, el servidor no se elevará, aunque admita la elevación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="b2e75-119">Si una clase COM con privilegios elevados usa la suplantación durante una llamada COM, podría perder sus privilegios elevados durante la suplantación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="b2e75-120">Si un servidor COM con privilegios elevados registra una clase en la tabla de objetos en ejecución (ROT), la clase no estará disponible para los clientes sin privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="b2e75-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="b2e75-121">Un proceso elevado mediante el uso del mecanismo de UAC no carga las clases por usuario durante las activaciones COM.</span><span class="sxs-lookup"><span data-stu-id="b2e75-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="b2e75-122">En el caso de las aplicaciones COM, esto significa que las clases COM de la aplicación deben instalarse en el subárbol del registro del **\_ \_ equipo local HKEY** si la aplicación va a ser utilizada por cuentas con privilegios y sin privilegios.</span><span class="sxs-lookup"><span data-stu-id="b2e75-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="b2e75-123">Las clases COM de la aplicación solo deben instalarse en el subárbol de **\_ usuarios HKEY** si la aplicación nunca la usan las cuentas con privilegios.</span><span class="sxs-lookup"><span data-stu-id="b2e75-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="b2e75-124">No se permite arrastrar y colocar desde aplicaciones no elevadas a elevadas.</span><span class="sxs-lookup"><span data-stu-id="b2e75-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e75-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2e75-125">Requirements</span></span>

<span data-ttu-id="b2e75-126">Para utilizar el moniker de elevación para activar una clase COM, se debe configurar la clase para que se ejecute como el usuario iniciador o la identidad de aplicación "activar como activador".</span><span class="sxs-lookup"><span data-stu-id="b2e75-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="b2e75-127">Si la clase está configurada para ejecutarse en cualquier otra identidad, la activación devuelve el error el valor en el CO \_ E \_ runas \_ \_ debe \_ ser \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="b2e75-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="b2e75-128">La clase también se debe anotar con un nombre para mostrar "descriptivo" que sea compatible con la interfaz de usuario multilingüe (MUI).</span><span class="sxs-lookup"><span data-stu-id="b2e75-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="b2e75-129">Esto requiere la siguiente entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="b2e75-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="b2e75-130">Si falta esta entrada, la activación devuelve el error CO \_ E \_ falta \_ DISPLAYNAME.</span><span class="sxs-lookup"><span data-stu-id="b2e75-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="b2e75-131">Si falta el archivo MUI, se devuelve el código de error de la función [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) .</span><span class="sxs-lookup"><span data-stu-id="b2e75-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="b2e75-132">Opcionalmente, para especificar el icono de la aplicación que va a mostrar la interfaz de usuario de UAC, agregue la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="b2e75-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="b2e75-133">**IconReference** usa el mismo formato que **LocalizedString**:</span><span class="sxs-lookup"><span data-stu-id="b2e75-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="b2e75-134">@*pathtobinary*,*-númerorecurso*</span><span class="sxs-lookup"><span data-stu-id="b2e75-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="b2e75-135">Además, el componente COM debe estar firmado para que se muestre el icono.</span><span class="sxs-lookup"><span data-stu-id="b2e75-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="b2e75-136">La clase COM también se debe anotar como habilitada para LUA.</span><span class="sxs-lookup"><span data-stu-id="b2e75-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="b2e75-137">Esto requiere la siguiente entrada del registro:</span><span class="sxs-lookup"><span data-stu-id="b2e75-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="b2e75-138">Si falta esta entrada, la activación devuelve la elevación del error CO \_ E \_ \_ deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="b2e75-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="b2e75-139">Tenga en cuenta que estas entradas deben existir en \_ el \_ subárbol del equipo local HKEY, no en el \_ \_ subárbol HKEY current user o HKEY \_ users.</span><span class="sxs-lookup"><span data-stu-id="b2e75-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="b2e75-140">Esto evita que los usuarios Eleven las clases COM que no tenían también los privilegios para registrarse.</span><span class="sxs-lookup"><span data-stu-id="b2e75-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="b2e75-141">El moniker de elevación y la interfaz de usuario de elevación</span><span class="sxs-lookup"><span data-stu-id="b2e75-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="b2e75-142">Si el cliente ya se ha elevado, el uso del moniker de elevación no hará que se muestre la interfaz de usuario de elevación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="b2e75-143">Cómo utilizar el moniker de elevación</span><span class="sxs-lookup"><span data-stu-id="b2e75-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="b2e75-144">El moniker de elevación es un moniker COM estándar, similar a los monikers de sesión, partición o cola.</span><span class="sxs-lookup"><span data-stu-id="b2e75-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="b2e75-145">Dirige una solicitud de activación a un servidor especificado con el nivel de elevación especificado.</span><span class="sxs-lookup"><span data-stu-id="b2e75-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="b2e75-146">El CLSID que se va a activar aparece en la cadena de moniker.</span><span class="sxs-lookup"><span data-stu-id="b2e75-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="b2e75-147">El moniker de elevación admite los siguientes tokens de nivel de ejecución:</span><span class="sxs-lookup"><span data-stu-id="b2e75-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="b2e75-148">Administrador</span><span class="sxs-lookup"><span data-stu-id="b2e75-148">Administrator</span></span>
2.  <span data-ttu-id="b2e75-149">Highest (el más alto)</span><span class="sxs-lookup"><span data-stu-id="b2e75-149">Highest</span></span>

<span data-ttu-id="b2e75-150">La sintaxis para esto es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2e75-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="b2e75-151">La sintaxis anterior usa el moniker "nuevo" para devolver una instancia de la clase COM especificada por *GUID*.</span><span class="sxs-lookup"><span data-stu-id="b2e75-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="b2e75-152">Tenga en cuenta que el moniker "nuevo" usa internamente la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) para obtener un objeto de clase y, a continuación, llama a [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) en él.</span><span class="sxs-lookup"><span data-stu-id="b2e75-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="b2e75-153">El moniker de elevación también se puede usar para obtener un objeto de clase, que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="b2e75-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="b2e75-154">A continuación, el llamador llama a [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para obtener una instancia de objeto.</span><span class="sxs-lookup"><span data-stu-id="b2e75-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="b2e75-155">La sintaxis para esto es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="b2e75-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="b2e75-156">Código de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b2e75-156">Sample code</span></span>

<span data-ttu-id="b2e75-157">En el ejemplo de código siguiente se muestra cómo utilizar el moniker de elevación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="b2e75-158">Se supone que ya se ha inicializado COM en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="b2e75-158">It assumes that you have already initialized COM on the current thread.</span></span>


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



<span data-ttu-id="b2e75-159">[**Enlazar \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) es una novedad de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2e75-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="b2e75-160">Se deriva de [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span><span class="sxs-lookup"><span data-stu-id="b2e75-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="b2e75-161">La única suma es un campo **hWnd** , **hWnd**.</span><span class="sxs-lookup"><span data-stu-id="b2e75-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="b2e75-162">Este identificador representa una ventana que se convierte en el propietario de la interfaz de usuario de elevación, si procede.</span><span class="sxs-lookup"><span data-stu-id="b2e75-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="b2e75-163">Si **hWnd** es **null**, com llamará a [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) para buscar un identificador de ventana asociado al subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="b2e75-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="b2e75-164">Este caso podría producirse si el cliente es un script, que no puede rellenar una estructura de [**enlace \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) .</span><span class="sxs-lookup"><span data-stu-id="b2e75-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="b2e75-165">En este caso, COM intentará usar la ventana asociada al subproceso de script.</span><span class="sxs-lookup"><span data-stu-id="b2e75-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="b2e75-166">Elevación sobre el hombro (OTS)</span><span class="sxs-lookup"><span data-stu-id="b2e75-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="b2e75-167">La elevación sobre el hombro (OTS) se refiere al escenario en el que un cliente ejecuta un servidor COM con las credenciales de un administrador en lugar de su propio.</span><span class="sxs-lookup"><span data-stu-id="b2e75-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="b2e75-168">(El término "sobre el hombro" significa que el administrador está inspeccionando el hombro del cliente mientras el cliente ejecuta el servidor).</span><span class="sxs-lookup"><span data-stu-id="b2e75-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="b2e75-169">Este escenario puede provocar un problema en las llamadas COM al servidor, ya que es posible que el servidor no llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explícitamente (es decir, mediante programación) o implícitamente (es decir, mediante declaración, con el registro).</span><span class="sxs-lookup"><span data-stu-id="b2e75-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="b2e75-170">En el caso de estos servidores, COM calcula un descriptor de seguridad que permite a los administradores de solo, del sistema y integrados \\ realizar llamadas com en el servidor.</span><span class="sxs-lookup"><span data-stu-id="b2e75-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="b2e75-171">Esta disposición no funcionará en escenarios de OTS.</span><span class="sxs-lookup"><span data-stu-id="b2e75-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="b2e75-172">En su lugar, el servidor debe llamar a **CoInitializeSecurity**, ya sea de forma explícita o implícita, y especificar una ACL que incluya el SID del grupo interactivo y el sistema.</span><span class="sxs-lookup"><span data-stu-id="b2e75-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="b2e75-173">En el ejemplo de código siguiente se muestra cómo crear un descriptor de seguridad (SD) con el SID de grupo interactivo.</span><span class="sxs-lookup"><span data-stu-id="b2e75-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

<span data-ttu-id="b2e75-174">En el ejemplo de código siguiente se muestra cómo llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implícitamente con el SD del ejemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="b2e75-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



<span data-ttu-id="b2e75-175">En el ejemplo de código siguiente se muestra cómo llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explícitamente con el SD anterior:</span><span class="sxs-lookup"><span data-stu-id="b2e75-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="b2e75-176">Permisos COM y etiquetas de acceso obligatorias</span><span class="sxs-lookup"><span data-stu-id="b2e75-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="b2e75-177">Windows Vista presenta el concepto de *etiquetas de acceso obligatorias* en los descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b2e75-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="b2e75-178">La etiqueta determina si los clientes pueden obtener acceso de ejecución a un objeto COM.</span><span class="sxs-lookup"><span data-stu-id="b2e75-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="b2e75-179">La etiqueta se especifica en la parte de la lista de control de acceso de sistema (SACL) del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b2e75-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="b2e75-180">En Windows Vista, COM es compatible con la etiqueta obligatoria del sistema etiqueta \_ \_ \_ \_ de no ejecutar \_ .</span><span class="sxs-lookup"><span data-stu-id="b2e75-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="b2e75-181">Las SACL de los permisos COM se omiten en los sistemas operativos anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2e75-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="b2e75-182">A partir de Windows Vista, dcomcnfg.exe no admite el cambio del nivel de integridad (IL) en los permisos COM.</span><span class="sxs-lookup"><span data-stu-id="b2e75-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="b2e75-183">Debe establecerse mediante programación.</span><span class="sxs-lookup"><span data-stu-id="b2e75-183">It must be set programmatically.</span></span>

<span data-ttu-id="b2e75-184">En el ejemplo de código siguiente se muestra cómo crear un descriptor de seguridad COM con una etiqueta que permite solicitudes de inicio o activación de todos los clientes de IL bajo.</span><span class="sxs-lookup"><span data-stu-id="b2e75-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="b2e75-185">Tenga en cuenta que las etiquetas son válidas para los permisos de inicio y activación, y de llamada.</span><span class="sxs-lookup"><span data-stu-id="b2e75-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="b2e75-186">Por lo tanto, es posible escribir un servidor COM que no permita el inicio, la activación o las llamadas de clientes con un determinado IL.</span><span class="sxs-lookup"><span data-stu-id="b2e75-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="b2e75-187">Para obtener más información acerca de los niveles de integridad, consulte la sección "Descripción del mecanismo de integridad de Windows Vista" en el tema [sobre cómo comprender y trabajar en modo protegido de Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b2e75-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="b2e75-188">CoCreateInstance y niveles de integridad</span><span class="sxs-lookup"><span data-stu-id="b2e75-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="b2e75-189">El comportamiento de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha cambiado en Windows Vista, para evitar que los clientes de Il bajo se enlacen a los servidores com de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b2e75-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="b2e75-190">El servidor debe permitir explícitamente dichos enlaces especificando la SACL.</span><span class="sxs-lookup"><span data-stu-id="b2e75-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="b2e75-191">Los cambios en **CoCreateInstance** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b2e75-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="b2e75-192">Al iniciar un proceso de servidor COM, el IL en el token de proceso de servidor se establece en el token de cliente o de servidor IL, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="b2e75-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="b2e75-193">De forma predeterminada, COM impedirá que los clientes de IL bajo se enlacen a las instancias en ejecución de cualquier servidor COM.</span><span class="sxs-lookup"><span data-stu-id="b2e75-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="b2e75-194">Para permitir el enlace, el descriptor de seguridad de inicio y activación de un servidor COM debe contener una SACL que especifique la etiqueta de IL bajo (consulte la sección anterior para ver el código de ejemplo para crear este tipo de descriptor de seguridad).</span><span class="sxs-lookup"><span data-stu-id="b2e75-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="b2e75-195">Servidores con privilegios elevados y registros de ROT</span><span class="sxs-lookup"><span data-stu-id="b2e75-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="b2e75-196">Si un servidor COM quiere registrarse en la tabla de objetos en ejecución (ROT) y permitir que cualquier cliente tenga acceso al registro, debe usar la \_ marca ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="b2e75-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="b2e75-197">Un servidor COM "activar como activador" no puede especificar ROTFLAGS \_ ALLOWANYCLIENT porque el administrador de control de servicios (DCOMSCM) de DCOM aplica una comprobación de suplantación de identidad en esta marca.</span><span class="sxs-lookup"><span data-stu-id="b2e75-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="b2e75-198">Por lo tanto, en Windows Vista, COM agrega compatibilidad con una nueva entrada del registro que permite al servidor estipular que los registros de la tabla ROT están disponibles para cualquier cliente:</span><span class="sxs-lookup"><span data-stu-id="b2e75-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="b2e75-199">El único valor válido para esta entrada de REG \_ DWORD es:</span><span class="sxs-lookup"><span data-stu-id="b2e75-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="b2e75-200">La entrada debe existir en el subárbol del **\_ \_ equipo local HKEY** .</span><span class="sxs-lookup"><span data-stu-id="b2e75-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="b2e75-201">Esta entrada proporciona un servidor "activar como activador" con la misma funcionalidad que ROTFLAGS \_ ALLOWANYCLIENT proporciona para un servidor runas.</span><span class="sxs-lookup"><span data-stu-id="b2e75-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2e75-202">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e75-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e75-203">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="b2e75-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

<span data-ttu-id="b2e75-204">[Descripción y trabajo con el modo protegido de Internet Explorer [puede estar en inglés]](/previous-versions/windows/internet-explorer/ie-developer/)</span><span class="sxs-lookup"><span data-stu-id="b2e75-204">[Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/)</span></span>
</dt> </dl>

 

 