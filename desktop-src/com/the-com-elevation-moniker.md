---
title: Moniker de elevación COM
description: El moniker de elevación COM permite que las aplicaciones que se ejecutan bajo el control de cuentas de usuario (UAC) activen clases COM con privilegios elevados. Para obtener más información, vea Centrarse en privilegios mínimos.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369768"
---
# <a name="the-com-elevation-moniker"></a>Moniker de elevación COM

El moniker de elevación COM permite que las aplicaciones que se ejecutan bajo el control de cuentas de usuario (UAC) activen clases COM con privilegios elevados. Para obtener más información, vea [Centrarse en privilegios mínimos.](/previous-versions/dotnet/articles/aa480194(v=msdn.10))

## <a name="when-to-use-the-elevation-moniker"></a>Cuándo usar el moniker de elevación

El moniker de elevación se usa para activar una clase COM para lograr una función específica y limitada que requiere privilegios elevados, como cambiar la fecha y hora del sistema.

La elevación requiere la participación de una clase COM y su cliente. La clase COM debe configurarse para admitir la elevación anotando su entrada del Registro, como se describe en la sección Requisitos. El cliente COM debe solicitar la elevación mediante el moniker de elevación.

El moniker de elevación no está diseñado para proporcionar compatibilidad con aplicaciones. Por ejemplo, si quieres ejecutar una aplicación COM heredada como WinWord como servidor con privilegios elevados, debes configurar el ejecutable del cliente COM para que requiera elevación, en lugar de activar la clase de la aplicación heredada con el moniker de elevación. Cuando el cliente COM con privilegios elevados llama a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) mediante el CLSID de la aplicación heredada, el estado elevado del cliente fluirá al proceso del servidor.

No toda la funcionalidad COM es compatible con la elevación. La funcionalidad que no funcionará incluye:

-   La elevación no fluye desde un cliente a un servidor COM remoto. Si un cliente activa un servidor COM remoto con el moniker de elevación, el servidor no se elevará, aunque admita la elevación.
-   Si una clase COM con privilegios elevados usa la suplantación durante una llamada COM, podría perder sus privilegios elevados durante la suplantación.
-   Si un servidor COM con privilegios elevados registra una clase en la tabla de objetos en ejecución (ROT), la clase no estará disponible para los clientes sin privilegios elevados.
-   Un proceso con privilegios elevados mediante el mecanismo UAC no carga clases por usuario durante las activaciones COM. Para las aplicaciones COM, esto significa que las clases COM de la aplicación deben instalarse en el subárbol del Registro **HKEY \_ LOCAL \_ MACHINE** si la aplicación se va a usar tanto en cuentas sin privilegios como en cuentas con privilegios. Las clases COM de la aplicación solo deben instalarse en el subárbol **HKEY \_ USERS** si las cuentas con privilegios nunca usan la aplicación.
-   No se permite arrastrar y colocar desde aplicaciones sin privilegios elevados a aplicaciones con privilegios elevados.

## <a name="requirements"></a>Requisitos

Para usar el moniker de elevación para activar una clase COM, la clase debe configurarse para ejecutarse como el usuario de inicio o la identidad de aplicación "Activate as Activator". Si la clase está configurada para ejecutarse con cualquier otra identidad, la activación devuelve el error CO \_ E \_ RUNAS \_ VALUE MUST \_ \_ BE \_ AAA.

La clase también debe anotarse con un nombre para mostrar "descriptivo" que sea compatible con la interfaz de usuario multilingüe (MUI). Esto requiere la siguiente entrada del Registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

Si falta esta entrada, la activación devuelve el error CO \_ E \_ MISSING \_ DISPLAYNAME. Si falta el archivo MUI, se devuelve el código de error [**de la función RegLoadMUIStringW.**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa)

Opcionalmente, para especificar un icono de aplicación que se mostrará mediante la interfaz de usuario de UAC, agregue la siguiente clave del Registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

**IconReference** usa el mismo formato que **LocalizedString**:

@*pathtobinary*,*-resourcenumber*

Además, el componente COM debe estar firmado para que se muestre el icono.

La clase COM también debe anotarse como HABILITADA PARA LUA. Esto requiere la siguiente entrada del Registro:

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

Si falta esta entrada, la activación devuelve el error CO \_ E \_ ELEVATION \_ DISABLED.

Tenga en cuenta que estas entradas deben existir en el subárbol HKEY LOCAL MACHINE, no en el subárbol \_ \_ HKEY \_ CURRENT USER o \_ HKEY \_ USERS. Esto evita que los usuarios eleven las clases COM que no tenían también los privilegios para registrarse.

## <a name="the-elevation-moniker-and-the-elevation-ui"></a>El Moniker de elevación y la interfaz de usuario de elevación

Si el cliente ya tiene privilegios elevados, el uso del moniker de elevación no hará que se muestre la interfaz de usuario de elevación.

## <a name="how-to-use-the-elevation-moniker"></a>Cómo usar el moniker de elevación

El moniker de elevación es un moniker COM estándar, similar a los monikers de sesión, partición o cola. Dirige una solicitud de activación a un servidor especificado con el nivel de elevación especificado. El CLSID que se va a activar aparece en la cadena del moniker.

El moniker de elevación admite los siguientes tokens de nivel de ejecución:

1.  Administrador
2.  Highest (el más alto)

La sintaxis para esto es la siguiente:

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

La sintaxis anterior usa el moniker "new" para devolver una instancia de la clase COM especificada por *guid*. Tenga en cuenta que el moniker "nuevo" usa internamente la interfaz [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) para obtener un objeto de clase y, a continuación, llama a [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) en él.

El moniker de elevación también se puede usar para obtener un objeto de clase, que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). A continuación, el autor de la llamada llama a [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para obtener una instancia de objeto. La sintaxis para esto es la siguiente:

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a>Código de ejemplo

En el ejemplo de código siguiente se muestra cómo usar el moniker de elevación. Se supone que ya ha inicializado COM en el subproceso actual.


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



[**BIND \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) es una novedad de Windows Vista. Se deriva de [**BIND \_ OPTS2.**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)

La única adición es **un campo HWND,** **hwnd**. Este identificador representa una ventana que se convierte en el propietario de la interfaz de usuario de elevación, si procede.

Si **hwnd** es **NULL,** COM llamará a [GetActiveWindow para](/windows/win32/api/winuser/nf-winuser-getactivewindow) buscar un identificador de ventana asociado al subproceso actual. Este caso puede producirse si el cliente es un script, que no puede rellenar una estructura [**BIND \_ OPTS3.**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) En este caso, COM intentará usar la ventana asociada al subproceso de script.

## <a name="over-the-shoulder-ots-elevation"></a>Elevación por encima del cuello (OTS)

La elevación por encima del cuello (OTS) hace referencia al escenario en el que un cliente ejecuta un servidor COM con las credenciales de un administrador en lugar de las suyas propias. (El término "encima del cuello" significa que el administrador está controlndo el cuello del cliente mientras el cliente ejecuta el servidor).

Este escenario podría causar un problema para las llamadas COM en el servidor, ya que es posible que el servidor no llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explícitamente (es decir, mediante programación) o implícitamente (es decir, mediante declaración, mediante el Registro). Para estos servidores, COM calcula un descriptor de seguridad que solo permite a los administradores SELF, SYSTEM y Builtin realizar llamadas \\ COM en el servidor. Esta disposición no funcionará en escenarios de OTS. En su lugar, el servidor debe llamar a **CoInitializeSecurity**, ya sea explícita o implícitamente, y especificar una ACL que incluya el SID del grupo INTERACTIVO y SYSTEM.

En el ejemplo de código siguiente se muestra cómo crear un descriptor de seguridad (SD) con el SID del grupo INTERACTIVO.

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

En el ejemplo de código siguiente se muestra cómo llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implícitamente con la SD del ejemplo de código anterior:


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



En el ejemplo de código siguiente se muestra cómo llamar a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explícitamente con la SD anterior:


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



## <a name="com-permissions-and-mandatory-access-labels"></a>Permisos COM y etiquetas de acceso obligatorio

Windows Vista presenta la noción de *etiquetas de acceso obligatorias en* los descriptores de seguridad. La etiqueta determina si los clientes pueden obtener acceso de ejecución a un objeto COM. La etiqueta se especifica en la parte de la lista de control de acceso del sistema (SACL) del descriptor de seguridad. En Windows Vista, COM admite la etiqueta SYSTEM \_ MANDATORY \_ LABEL NO \_ EXECUTE \_ \_ UP. Las SACL de los permisos COM se omiten en los sistemas operativos antes de Windows Vista.

A Windows Vista, dcomcnfg.exe no admite el cambio del nivel de integridad (IL) en los permisos COM. Debe establecerse mediante programación.

En el ejemplo de código siguiente se muestra cómo crear un descriptor de seguridad COM con una etiqueta que permite solicitudes de inicio y activación desde todos los clientes de LOW IL. Tenga en cuenta que las etiquetas son válidas para los permisos Launch/Activation y Call. Por lo tanto, es posible escribir un servidor COM que no permite el inicio, la activación o las llamadas de clientes con un IL determinado. Para obtener más información sobre los niveles de [integridad,](/previous-versions/windows/internet-explorer/ie-developer/)vea la sección "Understanding Windows Vista's Integrity Mechanism" (Descripción del mecanismo de integridad de Vista) en Understanding and Working in Protected Mode Internet Explorer .


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

El comportamiento de [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ha cambiado en Windows Vista, para evitar que los clientes de IL bajo se enlacen a servidores COM de forma predeterminada. El servidor debe permitir explícitamente dichos enlaces especificando la SACL. Los cambios en **CoCreateInstance** son los siguientes:

1.  Al iniciar un proceso de servidor COM, el IL del token de proceso de servidor se establece en el IL del token de cliente o servidor, lo que sea menor.
2.  De forma predeterminada, COM impedirá que los clientes de IL bajo enlacen a instancias en ejecución de cualquier servidor COM. Para permitir el enlace, el descriptor de seguridad Launch/Activation de un servidor COM debe contener una SACL que especifique la etiqueta il bajo (consulte la sección anterior para ver el código de ejemplo para crear un descriptor de seguridad de este tipo).

## <a name="elevated-servers-and-rot-registrations"></a>Servidores con privilegios elevados y registros ROT

Si un servidor COM desea registrarse en la tabla de objetos en ejecución (ROT) y permitir que cualquier cliente acceda al registro, debe usar la marca ROTFLAGS \_ ALLOWANYCLIENT. Un servidor COM "Activar como activador" no puede especificar ROTFLAGS ALLOWANYCLIENT porque el administrador de control de servicios DCOM (DCOMSCM) aplica una comprobación de suplantación de seguridad en esta \_ marca. Por lo tanto, en Windows Vista, COM agrega compatibilidad con una nueva entrada del Registro que permite al servidor estipular que sus registros ROT estén disponibles para cualquier cliente:

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

El único valor válido para esta entrada \_ REG DWORD es:

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

La entrada debe existir en el **subárbol HKEY \_ LOCAL \_ MACHINE.**

Esta entrada proporciona un servidor "Activar como activador" con la misma funcionalidad que ROTFLAGS \_ ALLOWANYCLIENT proporciona para un servidor RunAs.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad en COM](security-in-com.md)
</dt> <dt>

[Descripción y trabajo con el modo protegido de Internet Explorer [puede estar en inglés]](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 