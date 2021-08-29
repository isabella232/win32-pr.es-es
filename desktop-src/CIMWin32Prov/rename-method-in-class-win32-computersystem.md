---
description: Cambia el nombre de un equipo.
ms.assetid: 9d338ebe-caf0-42c4-995f-fd750e5664df
ms.tgt_platform: multiple
title: Método Rename de la Win32_ComputerSystem clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5f2a503cfac8e6cef8b32ee4e84cb8fa78f930d4e1126fcd0af488f3908c540f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077455"
---
# <a name="rename-method-of-the-win32_computersystem-class"></a>Método Rename de la clase ComputerSystem de Win32 \_

El **método Rename** cambia el nombre de un equipo.

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 Rename(
  [in] string Name,
  [in] string Password,
  [in] string UserName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Nuevo nombre de equipo. El valor de este parámetro no puede incluir caracteres de control, espacios iniciales o finales, ni ninguno de los caracteres siguientes: / \\ \\ \[ \] .

</dd> <dt>

*Contraseña* \[ En\]
</dt> <dd>

Contraseña que se usará al conectarse al controlador de dominio si el *parámetro UserName* especifica un nombre de cuenta. De lo contrario, este parámetro debe ser **NULL.** Vea la sección Comentarios de este tema para obtener más información sobre los *parámetros Password* *y UserName.*

</dd> <dt>

*UserName* \[ En\]
</dt> <dd>

Cadena que especifica el nombre de cuenta que se usará al conectarse al controlador de dominio. La cadena debe terminar en **null** y debe especificar un nombre NetBIOS de dominio y una cuenta de usuario, por ejemplo, "NOMBREDENOMBREDE DOMAIN" o ", que es un nombre principal de usuario \\ someone@domainname.com (UPN). Si el **parámetro UserName** es **NULL,** WMI usa el contexto del autor de la llamada. Vea la sección Comentarios de este tema para obtener más información sobre los *parámetros Password* *y UserName.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 (cero) si se realiza correctamente. Un valor devuelto distinto de cero indica un error. Si se realiza correctamente, se requiere un reinicio. Para obtener códigos de error adicionales, [**vea Wmi Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Para obtener valores **HRESULT** generales, vea [Códigos de error del sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Otros** (1 4294967295)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Puede usar el método **Rename** para cambiar el nombre de un equipo si es miembro del grupo de administradores local. Sin embargo, no puede usar el método de forma remota para los equipos de dominio.

Si se especifican los parámetros *Password* y *UserName,* la conexión a WMI debe usar el nivel de autenticación RPC **C \_ \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** **(wbemAuthenticationLevelPktPrivacy** para script y Visual Basic (VB)).

Para conectarse a un equipo remoto y especificar credenciales, use la conexión de objeto de localizador, que es IWbemLocator para C++, y SWbemLocator para script y VB. No use la conexión de moniker.

Para conectarse a un equipo local, no puede especificar una contraseña o una entidad de autenticación, como Kerberos. Solo puede especificar la contraseña y la entidad en las conexiones a equipos remotos.

Si el nivel de autenticación es demasiado bajo cuando se especifican Password y *UserName,* WMI devuelve el error **WBEM \_ E ENCRYPTED CONNECTION \_ \_ \_ REQUIRED** para C/C++, **y wbemErrEncryptedConnectionRequired** para script y VB. 

Para obtener más información, [**vea SWbemLocator \_ ConnectServer,**](/windows/desktop/WmiSdk/swbemlocator-connectserver)[**IWbemLocator::ConnectServer**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemlocator-connectserver)y [Constructing a Moniker String](/windows/desktop/WmiSdk/constructing-a-moniker-string).

## <a name="examples"></a>Ejemplos

El siguiente script muestra cómo cambiar el nombre de un equipo local.


```VB
Name = "name"
Password = "password"
Username = "username"

Set objWMIService = GetObject("Winmgmts:root\cimv2")

' Call always gets only one Win32_ComputerSystem object.
For Each objComputer in _
    objWMIService.InstancesOf("Win32_ComputerSystem")

        Return = objComputer.rename(Name,Password,Username)
        If Return <> 0 Then
           WScript.Echo "Rename failed. Error = " & Err.Number
        Else
           WScript.Echo "Rename succeeded." & _
               " Reboot for new name to go into effect"
        End If

Next
```



El siguiente ejemplo de código de C++ cambia el nombre de un sistema informático.


```C++
int set_computer_name(const string &newname/*, const string &username, const string &password*/)
{
 HRESULT hres;


// Step 1: --------------------------------------------------
 // Initialize COM. ------------------------------------------


hres = CoInitializeEx(0, COINIT_MULTITHREADED); 
 if (FAILED(hres))
 {
 cout << "Failed to initialize COM library. Error code = 0x" 
 << hex << hres << endl;
 return 1; // Program has failed.
 }


// Step 2: --------------------------------------------------
 // Set general COM security levels --------------------------
 // Note: If you are using Windows 2000, you need to specify -
 // the default authentication credentials for a user by using
 // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
 // parameter of CoInitializeSecurity ------------------------


hres = CoInitializeSecurity(
 NULL, 
 -1, // COM authentication
 NULL, // Authentication services
 NULL, // Reserved
 RPC_C_AUTHN_LEVEL_DEFAULT, // Default authentication 
 RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation 
 NULL, // Authentication info
 EOAC_NONE, // Additional capabilities 
 NULL // Reserved
 );




 if (FAILED(hres))
 {
 cout << "Failed to initialize security. Error code = 0x" 
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }

 // Step 3: ---------------------------------------------------
 // Obtain the initial locator to WMI -------------------------


IWbemLocator *pLoc = NULL;


hres = CoCreateInstance(
 CLSID_WbemLocator, 
 0, 
 CLSCTX_INPROC_SERVER, 
 IID_IWbemLocator, (LPVOID *) &pLoc);

 if (FAILED(hres))
 {
 cout << "Failed to create IWbemLocator object."
 << " Err code = 0x"
 << hex << hres << endl;
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 4: -----------------------------------------------------
 // Connect to WMI through the IWbemLocator::ConnectServer method


IWbemServices *pSvc = NULL;

 // Connect to the root\cimv2 namespace with
 // the current user and obtain pointer pSvc
 // to make IWbemServices calls.
 hres = pLoc->ConnectServer(
 _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
 NULL, // User name. NULL = current user
 NULL, // User password. NULL = current
 0, // Locale. NULL indicates current
 NULL, // Security flags.
 0, // Authority (e.g. Kerberos)
 0, // Context object 
 &pSvc // pointer to IWbemServices proxy
 );

 if (FAILED(hres))
 {
 cout << "Could not connect. Error code = 0x" 
 << hex << hres << endl;
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


/*cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;*/




 // Step 5: --------------------------------------------------
 // Set security levels on the proxy -------------------------


hres = CoSetProxyBlanket(
 pSvc, // Indicates the proxy to set
 RPC_C_AUTHN_WINNT, // RPC_C_AUTHN_xxx
 RPC_C_AUTHZ_NONE, // RPC_C_AUTHZ_xxx
 NULL, // Server principal name 
 RPC_C_AUTHN_LEVEL_CALL, // RPC_C_AUTHN_LEVEL_xxx 
 RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
 NULL, // client identity
 EOAC_NONE // proxy capabilities 
 );


if (FAILED(hres))
 {
 cout << "Could not set proxy blanket. Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release(); 
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 6: --------------------------------------------------
 // Use the IWbemServices pointer to make requests of WMI ----


// For example, get the name of the operating system
 IEnumWbemClassObject* pEnumerator = NULL;
 hres = pSvc->ExecQuery(
 bstr_t("WQL"), 
 bstr_t("SELECT * FROM Win32_ComputerSystem"),
 WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
 NULL,
 &pEnumerator);

 if (FAILED(hres))
 {
 cout << "Query for operating system name failed."
 << " Error code = 0x" 
 << hex << hres << endl;
 pSvc->Release();
 pLoc->Release();
 CoUninitialize();
 return 1; // Program has failed.
 }


// Step 7: -------------------------------------------------
 // Get the data from the query in step 6 -------------------

 IWbemClassObject *pclsObj;
 ULONG uReturn = 0;

 while (pEnumerator)
 {
 HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
 &pclsObj, &uReturn);


if(0 == uReturn)
 {
 break;
 }


// set up to call the Win32_ComputerSystem::Rename method
 BSTR MethodName = SysAllocString(L"Rename");
 BSTR ClassName = SysAllocString(L"Win32_ComputerSystem");


IWbemClassObject* pClass = NULL;
 hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);


IWbemClassObject* pInParamsDefinition = NULL;
 hres = pClass->GetMethod(MethodName, 0, 
 &pInParamsDefinition, NULL);


IWbemClassObject* pClassInstance = NULL;
 hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);


// Create the values for the in parameters
 wstring val;
 BSTR NewName;
 val.assign(newname.begin(), newname.end());
 NewName = SysAllocString(val.c_str());


VARIANT varName;
 varName.vt = VT_BSTR;
 varName.bstrVal = NewName;


// Store the value for the in parameters
 hres = pClassInstance->Put(L"Name", 0,
 &varName, 0);
 wprintf(L"Set computer name to %s\n", V_BSTR(&varName));


VARIANT var;
 CIMTYPE pType;
 LONG pFlavor;
 pclsObj->Get(L"__PATH",0,&var,&pType,&pFlavor);


// Execute Method
 IWbemClassObject* pOutParams = NULL;
 hres = pSvc->ExecMethod(var.bstrVal, MethodName, 0,
 NULL, pClassInstance, &pOutParams, NULL);


if (FAILED(hres))
 {
 cout << "Could not execute method. Error code = 0x" 
 << hex << hres << endl;
 VariantClear(&varName);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 1; // Program has failed.
 }


// To see what the method returned,
 // use the following code. The return value will
 // be in &varReturnValue
 VARIANT varReturnValue;
 hres = pOutParams->Get(_bstr_t(L"ReturnValue"), 0, 
 &varReturnValue, NULL, 0);




 // Clean up
 //--------------------------
 VariantClear(&varName);
 VariantClear(&varReturnValue);
 SysFreeString(ClassName);
 SysFreeString(MethodName);
 SysFreeString(NewName);
 pClass->Release();
 pInParamsDefinition->Release();
 pOutParams->Release();
 return 0;


}


// Cleanup
 // ========

 pSvc->Release();
 pLoc->Release();
 pEnumerator->Release();
 pclsObj->Release();
 CoUninitialize();


return 0; // Program successfully completed.
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Equipo \_ Win32System**](win32-computersystem.md)
</dt> <dt>

[Tareas wmi: cuentas y dominios](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> </dl>

 

