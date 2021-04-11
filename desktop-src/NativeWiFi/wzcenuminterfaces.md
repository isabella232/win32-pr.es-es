---
description: Enumera todas las interfaces LAN inalámbricas administradas por el servicio de configuración inalámbrica cero.
ms.assetid: ef8a6a3e-042a-4219-baed-a82bb3e983ae
title: Función WZCEnumInterfaces (wzcsapi. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912518"
---
# <a name="wzcenuminterfaces-function"></a><span data-ttu-id="0a600-103">WZCEnumInterfaces función)</span><span class="sxs-lookup"><span data-stu-id="0a600-103">WZCEnumInterfaces function</span></span>

<span data-ttu-id="0a600-104">\[**WZCEnumInterfaces** ya no es compatible con Windows Vista y windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="0a600-104">\[**WZCEnumInterfaces** is no longer supported as of Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="0a600-105">En su lugar, use la función [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) .</span><span class="sxs-lookup"><span data-stu-id="0a600-105">Instead, use the [**WlanEnumInterfaces**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces) function.</span></span> <span data-ttu-id="0a600-106">Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]</span><span class="sxs-lookup"><span data-stu-id="0a600-106">For more information, see [About the Native Wifi API](about-the-native-wifi-api.md).\]</span></span>

<span data-ttu-id="0a600-107">La función **WZCEnumInterfaces** enumera todas las interfaces LAN inalámbricas administradas por el servicio de configuración inalámbrica rápida.</span><span class="sxs-lookup"><span data-stu-id="0a600-107">The **WZCEnumInterfaces** function enumerates all of the wireless LAN interfaces managed by the Wireless Zero Configuration service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a600-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a600-108">Syntax</span></span>


```C++
DWORD WZCEnumInterfaces(
  _In_  LPWSTR           pSrvAddr,
  _Out_ PINTFS_KEY_TABLE pIntfs
);
```



## <a name="parameters"></a><span data-ttu-id="0a600-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a600-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a600-110">*pSrvAddr* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a600-110">*pSrvAddr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a600-111">Puntero a una cadena que contiene el nombre del equipo en el que se va a ejecutar esta función.</span><span class="sxs-lookup"><span data-stu-id="0a600-111">A pointer to a string containing the name of the computer on which to execute this function.</span></span> <span data-ttu-id="0a600-112">Si este parámetro es **null**, el servicio de configuración inalámbrica cero se enumera en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="0a600-112">If this parameter is **NULL**, then the Wireless Zero Configuration service is enumerated on the local computer.</span></span>

<span data-ttu-id="0a600-113">Si el parámetro *pSrvAddr* especificado es un equipo remoto, el equipo remoto debe admitir llamadas RPC remotas.</span><span class="sxs-lookup"><span data-stu-id="0a600-113">If the *pSrvAddr* parameter specified is a remote computer, then the remote computer must support remote RPC calls.</span></span>

</dd> <dt>

<span data-ttu-id="0a600-114">*pIntfs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0a600-114">*pIntfs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a600-115">Puntero a una estructura [**de \_ \_ tabla de claves de INTFS**](intfs-key-table.md) que contiene una tabla de información de clave para todas las interfaces.</span><span class="sxs-lookup"><span data-stu-id="0a600-115">A pointer to a [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure that contains a table of key information for all interfaces.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a600-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a600-116">Return value</span></span>

<span data-ttu-id="0a600-117">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="0a600-117">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0a600-118">Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="0a600-118">If the function fails, the return value may be one of the following return codes.</span></span>



| <span data-ttu-id="0a600-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0a600-119">Return code</span></span>                                                                                               | <span data-ttu-id="0a600-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0a600-120">Description</span></span>                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a600-121"><dt>**ERROR de la \_ arena \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-121"><dt>**ERROR\_ARENA\_TRASHED**</dt></span></span> </dl>      | <span data-ttu-id="0a600-122">Los bloques de control de almacenamiento se han destruido.</span><span class="sxs-lookup"><span data-stu-id="0a600-122">The storage control blocks were destroyed.</span></span> <span data-ttu-id="0a600-123">Se devuelve este error si el servicio de configuración inalámbrica cero no ha inicializado objetos internos.</span><span class="sxs-lookup"><span data-stu-id="0a600-123">This error is returned if the Wireless Zero Configuration service has not initialized internal objects.</span></span><br/> |
| <dl> <span data-ttu-id="0a600-124"><dt>**RPC \_ S \_ desconocido \_ si**</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-124"><dt>**RPC\_S\_UNKNOWN\_IF**</dt></span></span> </dl>        | <span data-ttu-id="0a600-125">Se desconoce la interfaz.</span><span class="sxs-lookup"><span data-stu-id="0a600-125">The interface is unknown.</span></span><br/> <span data-ttu-id="0a600-126">Se devuelve este error si no se inicia el servicio de configuración inalámbrica cero.</span><span class="sxs-lookup"><span data-stu-id="0a600-126">This error is returned if the Wireless Zero Configuration service is not started.</span></span><br/>                             |
| <dl> <span data-ttu-id="0a600-127"><dt>**\_puntero de \_ \_ referencia null \_ de RPC X**</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-127"><dt>**RPC\_X\_NULL\_REF\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="0a600-128">Se pasó un puntero de referencia nulo al código auxiliar.</span><span class="sxs-lookup"><span data-stu-id="0a600-128">A null reference pointer was passed to the stub.</span></span><br/> <span data-ttu-id="0a600-129">Se devuelve este error si el parámetro *pIntfs* es **null**.</span><span class="sxs-lookup"><span data-stu-id="0a600-129">This error is returned if the *pIntfs* parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="0a600-130"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-130"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="0a600-131">No hay suficiente memoria disponible para procesar esta solicitud y asignar memoria para los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="0a600-131">Not enough memory is available to process this request and allocate memory for the query results.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="0a600-132"><dt>**Estado de RPC \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-132"><dt>**RPC\_STATUS**</dt></span></span> </dl>                | <span data-ttu-id="0a600-133">Varios códigos de error.</span><span class="sxs-lookup"><span data-stu-id="0a600-133">Various error codes.</span></span><br/>                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="0a600-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a600-134">Remarks</span></span>

<span data-ttu-id="0a600-135">El miembro **dwNumIntfs** de la estructura de la [**\_ \_ tabla de claves INTFS**](intfs-key-table.md) a la que apunta *pIntf* debe establecerse en 0 antes de llamar a la función **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="0a600-135">The **dwNumIntfs** member of the [**INTFS\_KEY\_TABLE**](intfs-key-table.md) structure pointed to by *pIntf* must be set to 0 before calling the **WZCEnumInterfaces** function.</span></span> <span data-ttu-id="0a600-136">Además, el miembro **pIntfs** debe establecerse en **null**.</span><span class="sxs-lookup"><span data-stu-id="0a600-136">Also, the **pIntfs** member must be set to **NULL**.</span></span>

<span data-ttu-id="0a600-137">En el caso de las llamadas posteriores a otras funciones de configuración inalámbricas cero, una aplicación debe identificar la interfaz en la que está funcionando proporcionando la información de clave pertinente devuelta por la función **WZCEnumInterfaces** .</span><span class="sxs-lookup"><span data-stu-id="0a600-137">For subsequent calls to other Wireless Zero Configuration functions, an application must identify the interface it is operating on by providing relevant key information returned by the **WZCEnumInterfaces** function.</span></span>

<span data-ttu-id="0a600-138">Si **WZCEnumInterfaces** devuelve un error \_ , el llamador debe llamar a [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) para liberar los búferes internos asignados para los datos devueltos cuando ya no se necesite esta información.</span><span class="sxs-lookup"><span data-stu-id="0a600-138">If the **WZCEnumInterfaces** returns ERROR\_SUCCESS, the caller should call [**LocalFree**](/windows/win32/api/winbase/nf-winbase-localfree) to release the internal buffers allocated for the data returned once this information is no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="0a600-139">El archivo de encabezado *wzcsapi. h* y el archivo de biblioteca de importación *wzcsapi. lib* no están disponibles en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0a600-139">The *Wzcsapi.h* header file and *Wzcsapi.lib* import library file are not available in the Windows SDK.</span></span>

 

## <a name="examples"></a><span data-ttu-id="0a600-140">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0a600-140">Examples</span></span>

<span data-ttu-id="0a600-141">En el ejemplo siguiente se enumeran las interfaces LAN inalámbricas en el equipo local administrado por el servicio de configuración inalámbrica cero y se imprime el valor de la interfaz GUID para cada interfaz.</span><span class="sxs-lookup"><span data-stu-id="0a600-141">The following example enumerates the wireless LAN interfaces on the local computer managed by the Wireless Zero Configuration service and prints out the value for interface GUID for each interface.</span></span>

> [!Note]  
> <span data-ttu-id="0a600-142">En este ejemplo se producirá un error en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="0a600-142">This example will fail on Windows Vista and later .</span></span>

 


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



## <a name="requirements"></a><span data-ttu-id="0a600-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a600-143">Requirements</span></span>



| <span data-ttu-id="0a600-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a600-144">Requirement</span></span> | <span data-ttu-id="0a600-145">Value</span><span class="sxs-lookup"><span data-stu-id="0a600-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a600-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a600-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0a600-147">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a600-147">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0a600-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a600-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0a600-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a600-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0a600-150">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="0a600-150">End of client support</span></span><br/>    | <span data-ttu-id="0a600-151">Windows XP con SP3</span><span class="sxs-lookup"><span data-stu-id="0a600-151">Windows XP with SP3</span></span><br/>                                                         |
| <span data-ttu-id="0a600-152">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0a600-152">End of server support</span></span><br/>    | <span data-ttu-id="0a600-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0a600-153">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0a600-154">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0a600-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a600-155"><dt>Wzcsapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-155"><dt>Wzcsapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a600-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a600-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a600-157"><dt>Wzcsapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-157"><dt>Wzcsapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a600-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a600-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a600-159"><dt>Wzcsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a600-159"><dt>Wzcsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a600-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a600-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a600-161">**\_tabla de claves de INTFS \_**</span><span class="sxs-lookup"><span data-stu-id="0a600-161">**INTFS\_KEY\_TABLE**</span></span>](intfs-key-table.md)
</dt> <dt>

[<span data-ttu-id="0a600-162">**\_entrada de clave de Intf \_**</span><span class="sxs-lookup"><span data-stu-id="0a600-162">**INTF\_KEY\_ENTRY**</span></span>](intf-key-entry.md)
</dt> <dt>

[<span data-ttu-id="0a600-163">**WZCEapolGetInterfaceParams**</span><span class="sxs-lookup"><span data-stu-id="0a600-163">**WZCEapolGetInterfaceParams**</span></span>](wzceapolgetinterfaceparams.md)
</dt> <dt>

[<span data-ttu-id="0a600-164">**WZCQueryInterface**</span><span class="sxs-lookup"><span data-stu-id="0a600-164">**WZCQueryInterface**</span></span>](wzcqueryinterface.md)
</dt> <dt>

[<span data-ttu-id="0a600-165">**WZCRefreshInterface**</span><span class="sxs-lookup"><span data-stu-id="0a600-165">**WZCRefreshInterface**</span></span>](wzcrefreshinterface.md)
</dt> </dl>

 

 
