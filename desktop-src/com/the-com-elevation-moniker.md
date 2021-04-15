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
# <a name="the-com-elevation-moniker"></a>Moniker de elevación COM

El moniker de elevación de COM permite a las aplicaciones que se ejecutan en control de cuentas de usuario (UAC) activar las clases COM con privilegios elevados. Para obtener más información, consulte [enfoque de privilegios mínimos](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).

## <a name="when-to-use-the-elevation-moniker"></a>Cuándo utilizar el moniker de elevación

El moniker de elevación se utiliza para activar una clase COM con el fin de lograr una función específica y limitada que requiere privilegios elevados, como cambiar la fecha y la hora del sistema.

La elevación requiere la participación de una clase COM y su cliente. La clase COM se debe configurar para admitir la elevación mediante la anotación de la entrada del registro, como se describe en la sección requisitos. El cliente COM debe solicitar la elevación mediante el moniker de elevación.

El moniker de elevación no está diseñado para proporcionar compatibilidad con aplicaciones. Por ejemplo, si desea ejecutar una aplicación COM heredada como WinWord como servidor con privilegios elevados, debe configurar el ejecutable del cliente COM para que requiera elevación, en lugar de activar la clase de la aplicación heredada con el moniker de elevación. Cuando el cliente COM con privilegios elevados llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mediante el CLSID de la aplicación heredada, el estado elevado del cliente pasará al proceso del servidor.

No toda la funcionalidad de COM es compatible con la elevación. Entre las funciones que no funcionarán se incluyen:

-   La elevación no fluye desde un cliente a un servidor COM remoto. Si un cliente activa un servidor COM remoto con el moniker de elevación, el servidor no se elevará, aunque admita la elevación.
-   Si una clase COM con privilegios elevados usa la suplantación durante una llamada COM, podría perder sus privilegios elevados durante la suplantación.
-   Si un servidor COM con privilegios elevados registra una clase en la tabla de objetos en ejecución (ROT), la clase no estará disponible para los clientes sin privilegios elevados.
-   Un proceso elevado mediante el uso del mecanismo de UAC no carga las clases por usuario durante las activaciones COM. En el caso de las aplicaciones COM, esto significa que las clases COM de la aplicación deben instalarse en el subárbol del registro del **\_ \_ equipo local HKEY** si la aplicación va a ser utilizada por cuentas con privilegios y sin privilegios. Las clases COM de la aplicación solo deben instalarse en el subárbol de **\_ usuarios HKEY** si la aplicación nunca la usan las cuentas con privilegios.
-   No se permite arrastrar y colocar desde aplicaciones no elevadas a elevadas.

## <a name="requirements"></a>Requisitos

Para utilizar el moniker de elevación para activar una clase COM, se debe configurar la clase para que se ejecute como el usuario iniciador o la identidad de aplicación "activar como activador". Si la clase está configurada para ejecutarse en cualquier otra identidad, la activación devuelve el error el valor en el CO \_ E \_ runas \_ \_ debe \_ ser \_ AAA.

La clase también se debe anotar con un nombre para mostrar "descriptivo" que sea compatible con la interfaz de usuario multilingüe (MUI). Esto requiere la siguiente entrada del registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Si falta esta entrada, la activación devuelve el error CO \_ E \_ falta \_ DISPLAYNAME. Si falta el archivo MUI, se devuelve el código de error de la función [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) .

Opcionalmente, para especificar el icono de la aplicación que va a mostrar la interfaz de usuario de UAC, agregue la siguiente clave del registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** usa el mismo formato que **LocalizedString**:

@*pathtobinary*,*-númerorecurso*

Además, el componente COM debe estar firmado para que se muestre el icono.

La clase COM también se debe anotar como habilitada para LUA. Esto requiere la siguiente entrada del registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Si falta esta entrada, la activación devuelve la elevación del error CO \_ E \_ \_ deshabilitada.

Tenga en cuenta que estas entradas deben existir en \_ el \_ subárbol del equipo local HKEY, no en el \_ \_ subárbol HKEY current user o HKEY \_ users. Esto evita que los usuarios Eleven las clases COM que no tenían también los privilegios para registrarse.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>El moniker de elevación y la interfaz de usuario de elevación

Si el cliente ya se ha elevado, el uso del moniker de elevación no hará que se muestre la interfaz de usuario de elevación.

## <a name="how-to-use-the-elevation-moniker"></a>Cómo utilizar el moniker de elevación

El moniker de elevación es un moniker COM estándar, similar a los monikers de sesión, partición o cola. Dirige una solicitud de activación a un servidor especificado con el nivel de elevación especificado. El CLSID que se va a activar aparece en la cadena de moniker.

El moniker de elevación admite los siguientes tokens de nivel de ejecución:

1.  Administrador
2.  Highest (el más alto)

La sintaxis para esto es la siguiente:

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

La sintaxis anterior usa el moniker "nuevo" para devolver una instancia de la clase COM especificada por *GUID*. Tenga en cuenta que el moniker "nuevo" usa internamente la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) para obtener un objeto de clase y, a continuación, llama a [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) en él.

El moniker de elevación también se puede usar para obtener un objeto de clase, que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). A continuación, el llamador llama a [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para obtener una instancia de objeto. La sintaxis para esto es la siguiente:

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Código de ejemplo

En el ejemplo de código siguiente se muestra cómo utilizar el moniker de elevación. Se supone que ya se ha inicializado COM en el subproceso actual.


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



[**Enlazar \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) es una novedad de Windows Vista. Se deriva de [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).

La única suma es un campo **hWnd** , **hWnd**. Este identificador representa una ventana que se convierte en el propietario de la interfaz de usuario de elevación, si procede.

Si **hWnd** es **null**, com llamará a [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) para buscar un identificador de ventana asociado al subproceso actual. Este caso podría producirse si el cliente es un script, que no puede rellenar una estructura de [**enlace \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) . En este caso, COM intentará usar la ventana asociada al subproceso de script.

## <a name="over-the-shoulder-ots-elevation"></a>Elevación sobre el hombro (OTS)

La elevación sobre el hombro (OTS) se refiere al escenario en el que un cliente ejecuta un servidor COM con las credenciales de un administrador en lugar de su propio. (El término "sobre el hombro" significa que el administrador está inspeccionando el hombro del cliente mientras el cliente ejecuta el servidor).

Este escenario puede provocar un problema en las llamadas COM al servidor, ya que es posible que el servidor no llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explícitamente (es decir, mediante programación) o implícitamente (es decir, mediante declaración, con el registro). En el caso de estos servidores, COM calcula un descriptor de seguridad que permite a los administradores de solo, del sistema y integrados \\ realizar llamadas com en el servidor. Esta disposición no funcionará en escenarios de OTS. En su lugar, el servidor debe llamar a **CoInitializeSecurity**, ya sea de forma explícita o implícita, y especificar una ACL que incluya el SID del grupo interactivo y el sistema.

En el ejemplo de código siguiente se muestra cómo crear un descriptor de seguridad (SD) con el SID de grupo interactivo.

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

En el ejemplo de código siguiente se muestra cómo llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implícitamente con el SD del ejemplo de código anterior:


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



En el ejemplo de código siguiente se muestra cómo llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explícitamente con el SD anterior:


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



## <a name="com-permissions-and-mandatory-access-labels"></a>Permisos COM y etiquetas de acceso obligatorias

Windows Vista presenta el concepto de *etiquetas de acceso obligatorias* en los descriptores de seguridad. La etiqueta determina si los clientes pueden obtener acceso de ejecución a un objeto COM. La etiqueta se especifica en la parte de la lista de control de acceso de sistema (SACL) del descriptor de seguridad. En Windows Vista, COM es compatible con la etiqueta obligatoria del sistema etiqueta \_ \_ \_ \_ de no ejecutar \_ . Las SACL de los permisos COM se omiten en los sistemas operativos anteriores a Windows Vista.

A partir de Windows Vista, dcomcnfg.exe no admite el cambio del nivel de integridad (IL) en los permisos COM. Debe establecerse mediante programación.

En el ejemplo de código siguiente se muestra cómo crear un descriptor de seguridad COM con una etiqueta que permite solicitudes de inicio o activación de todos los clientes de IL bajo. Tenga en cuenta que las etiquetas son válidas para los permisos de inicio y activación, y de llamada. Por lo tanto, es posible escribir un servidor COM que no permita el inicio, la activación o las llamadas de clientes con un determinado IL. Para obtener más información acerca de los niveles de integridad, consulte la sección "Descripción del mecanismo de integridad de Windows Vista" en el tema [sobre cómo comprender y trabajar en modo protegido de Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).


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



## <a name="cocreateinstance-and-integrity-levels"></a>CoCreateInstance y niveles de integridad

El comportamiento de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha cambiado en Windows Vista, para evitar que los clientes de Il bajo se enlacen a los servidores com de forma predeterminada. El servidor debe permitir explícitamente dichos enlaces especificando la SACL. Los cambios en **CoCreateInstance** son los siguientes:

1.  Al iniciar un proceso de servidor COM, el IL en el token de proceso de servidor se establece en el token de cliente o de servidor IL, lo que sea menor.
2.  De forma predeterminada, COM impedirá que los clientes de IL bajo se enlacen a las instancias en ejecución de cualquier servidor COM. Para permitir el enlace, el descriptor de seguridad de inicio y activación de un servidor COM debe contener una SACL que especifique la etiqueta de IL bajo (consulte la sección anterior para ver el código de ejemplo para crear este tipo de descriptor de seguridad).

## <a name="elevated-servers-and-rot-registrations"></a>Servidores con privilegios elevados y registros de ROT

Si un servidor COM quiere registrarse en la tabla de objetos en ejecución (ROT) y permitir que cualquier cliente tenga acceso al registro, debe usar la \_ marca ROTFLAGS ALLOWANYCLIENT. Un servidor COM "activar como activador" no puede especificar ROTFLAGS \_ ALLOWANYCLIENT porque el administrador de control de servicios (DCOMSCM) de DCOM aplica una comprobación de suplantación de identidad en esta marca. Por lo tanto, en Windows Vista, COM agrega compatibilidad con una nueva entrada del registro que permite al servidor estipular que los registros de la tabla ROT están disponibles para cualquier cliente:

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

El único valor válido para esta entrada de REG \_ DWORD es:

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

La entrada debe existir en el subárbol del **\_ \_ equipo local HKEY** .

Esta entrada proporciona un servidor "activar como activador" con la misma funcionalidad que ROTFLAGS \_ ALLOWANYCLIENT proporciona para un servidor runas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[Descripción y trabajo con el modo protegido de Internet Explorer [puede estar en inglés]](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 