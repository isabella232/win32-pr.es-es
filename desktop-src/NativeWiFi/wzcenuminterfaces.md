---
description: Enumera todas las interfaces laN inalámbricas administradas por el servicio Configuración inalámbrica cero.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: Función WZCEnumInterfaces (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEnumInterfaces
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: b2a2c886f59843dd1bf1316053c603faf4cc112a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169389"
---
# <a name="wzcenuminterfaces-function"></a>Función WZCEnumInterfaces

\[**WZCEnumInterfaces** ya no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [**la función WlanEnumInterfaces.**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) Para obtener más información, vea [Acerca de la API de Wi-Fi nativa.](about-the-native-wifi-api.md)\]

La **función WZCEnumInterfaces** enumera todas las interfaces LAN inalámbricas administradas por el servicio configuración inalámbrica cero.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSrvAddr* \[ En\]
</dt> <dd>

Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función. Si este parámetro es **NULL,** el servicio configuración inalámbrica cero se enumera en el equipo local.

Si el *parámetro pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.

</dd> <dt>

*pIntfs* \[ out\]
</dt> <dd>

Puntero a una [**estructura INTFS \_ KEY \_ TABLE**](intfs-key-table.md) que contiene una tabla de información clave para todas las interfaces.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.



| Código devuelto                                                                                               | Descripción                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERROR \_ DE LA \_ PAPELERA**</dt> </dl>      | Los bloques de control de almacenamiento se destruyeron. Este error se devuelve si el servicio configuración inalámbrica cero no ha inicializado objetos internos.<br/> |
| <dl> <dt>**RPC \_ S \_ UNKNOWN \_ IF**</dt> </dl>        | La interfaz es desconocida.<br/> Este error se devuelve si no se inicia el servicio configuración inalámbrica cero.<br/>                             |
| <dl> <dt>**RPC \_ X \_ NULL \_ REF \_ POINTER**</dt> </dl> | Se pasó un puntero de referencia null al código auxiliar.<br/> Este error se devuelve si el *parámetro pIntfs* es **NULL.**<br/>                          |
| <dl> <dt>**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**</dt> </dl> | No hay suficiente memoria disponible para procesar esta solicitud y asignar memoria para los resultados de la consulta.<br/>                                                  |
| <dl> <dt>**ESTADO \_ RPC**</dt> </dl>                | Varios códigos de error.<br/>                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

El **miembro dwNumIntfs** de la estructura [**INTFS \_ KEY \_ TABLE**](intfs-key-table.md) a la que apunta *pIntf* debe establecerse en 0 antes de llamar a la función **WZCEnumInterfaces.** Además, el **miembro pIntfs** debe establecerse en **NULL.**

Para las llamadas posteriores a otras funciones de configuración inalámbrica cero, una aplicación debe identificar la interfaz en la que está funcionando proporcionando la información clave pertinente devuelta por la función **WZCEnumInterfaces.**

Si **WZCEnumInterfaces** devuelve ERROR SUCCESS, el autor de la llamada debe llamar a LocalFree para liberar los búferes internos asignados para los datos devueltos una vez que esta información ya no sea \_ necesaria. [](/windows/win32/api/winbase/nf-winbase-localfree)

> [!Note]  
> El *archivo de encabezado Wzcsapi.h* y el archivo de biblioteca de importación *Wzcsapi.lib* no están disponibles en Windows SDK.

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se enumeran las interfaces laN inalámbricas en el equipo local administrado por el servicio configuración inalámbrica cero e imprime el valor del GUID de interfaz para cada interfaz.

> [!Note]  
> Este ejemplo producirá un error en Windows Vista y versiones posteriores.

 


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <objbase.h>
#include <wtypes.h>

#include <stdio.h>
#include <stdlib.h>

// Wzcsapi.h and Wsczapi.lib were never shipped
// So we need to LOadlibrary and call the WZCEnumInterfaces function 
// in Wzcsapi.dll in the 

typedef struct
{
    LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;

typedef struct
{
    DWORD dwNumIntfs;
    PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;

DWORD WZCEnumInterfaces(LPWSTR pSrvAddr, PINTFS_KEY_TABLE pIntfs);

//Define the function prototype
typedef DWORD (CALLBACK* WZCEnumInterfacesType)(LPWSTR, PINTFS_KEY_TABLE);

int wmain()
{
    // Declare and initialize variables.

    DWORD dwResult = 0;
//    int iRet = 0;
    
//    WCHAR GuidString[40] = {0};
     
    int i;

    /* variables used for WZCEnumInterfaces  */
    
    PINTFS_KEY_TABLE pIfList; 
    PINTF_KEY_ENTRY pIfInfo;
    
    BOOL freeResult = FALSE;
    BOOL runTimeLinkSuccess = FALSE; 
    HINSTANCE dllHandle = NULL;              
    WZCEnumInterfacesType WZCEnumInterfacesPtr = NULL;

//    wprintf(L"Sample to test WZCEnumInterface\n");
    
    //Load the dll and keep the handle to it
    dllHandle = LoadLibrary( (LPCWSTR) L"wzcsapi.dll");

    // If the handle is valid, try to get the function address. 
    if (dllHandle == NULL) {
        dwResult = GetLastError();
        wprintf(L"LoadLibrary of wzcsapi.dll failed with error: %d\n", dwResult);
        if (dwResult ==  ERROR_MOD_NOT_FOUND)
            wprintf(L"Error: The specified module could not be found\n");
        return 1;
    }
    else  
    { 
        //Get pointer to our function using GetProcAddress:
        WZCEnumInterfacesPtr = (WZCEnumInterfacesType) GetProcAddress(dllHandle,
         "WZCEnumInterfaces");

        if (WZCEnumInterfacesPtr != NULL)
            runTimeLinkSuccess = TRUE;
        else {
            dwResult = GetLastError();   
            wprintf(L"GetProcAddress of WZCEnumInterfaces failed with error: %d\n", dwResult);
            return 1;
        }    
             
        // The function address is valid, allocate some memory for pIflist
        pIfList = (PINTFS_KEY_TABLE) LocalAlloc(LMEM_ZEROINIT,4096);
        if (pIfList == NULL) {    
            wprintf(L"Unable to allocate memory to store INTFS_KEY_TABLE\n");
            freeResult = FreeLibrary(dllHandle);
            return 1;
        }    

        // If the function address is valid, call the function. 
        if (runTimeLinkSuccess)
        {
            dwResult = WZCEnumInterfacesPtr(NULL, pIfList); 
            if (dwResult != ERROR_SUCCESS)  {
                wprintf(L"WZCEnumInterfaces failed with error: %u\n", dwResult);
                // FormatMessage can be used to find out why the function failed
                  //Free the library:
                freeResult = FreeLibrary(dllHandle);
                return 1;
            }
            else {
                wprintf(L"Num Entries: %lu\n", pIfList->dwNumIntfs);

                for (i = 0; i < (int) pIfList->dwNumIntfs; i++) {
                    pIfInfo = &pIfList->pIntfs[i];
                    if (pIfInfo->wszGuid == NULL)
                        wprintf(L"  InterfaceGUID[%d]: NULL\n",i);
                    else
                        wprintf(L"  InterfaceGUID[%d]: %ws\n",i, pIfInfo->wszGuid);
                    
                }    
            }
            wprintf(L"\n");
        }
        
        freeResult = FreeLibrary(dllHandle);
    }

    if (pIfList != NULL) {
        LocalFree(pIfList);
        pIfList = NULL;
    }
    return 0;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                         |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Wzcsapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TABLA DE CLAVES \_ \_ INTFS**](intfs-key-table.md)
</dt> <dt>

[**ENTRADA DE \_ CLAVE \_ INTF**](intf-key-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
