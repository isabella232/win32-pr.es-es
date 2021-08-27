---
title: Enumeración de controladores de dominio
description: En versiones anteriores de Windows, una aplicación solo podía obtener un controlador de dominio único en un dominio mediante una llamada a DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory , enumeración de controladores de dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54234301ad843708fd4e9b20e38f2b4fd8391e1134a78cea8b0d45a001d701d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695153"
---
# <a name="enumerating-domain-controllers"></a>Enumeración de controladores de dominio

En versiones anteriores de Windows, una aplicación solo podía obtener un controlador de dominio único en un dominio mediante una llamada a [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). No había ninguna manera de predecir qué controlador de dominio se recuperaría ni obtener una lista de los controladores de dominio. Windows permite que una aplicación enumere los controladores de dominio de un dominio mediante las funciones [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)y [**DsGetDcClose.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)

Para enumerar un controlador de dominio, llame a [**DsGetDcOpen.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) Esta función toma parámetros que definen el dominio para enumerar y otras opciones de enumeración. **DsGetDcOpen** proporciona un identificador de contexto de enumeración de dominio que se usa para identificar la operación de enumeración cuando se llama a [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) y [**DsGetDcClose.**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew)

Se [**llama a la función DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) con el identificador de contexto de enumeración de dominio para recuperar el siguiente controlador de dominio en la enumeración. La primera vez que se llama a esta función, se recupera el primer controlador de dominio de la enumeración . La segunda vez que se llama a esta función, se recupera el segundo controlador de dominio de la enumeración . Este proceso se repite hasta **que DsGetDcNext** devuelve **ERROR NO MORE \_ \_ \_ ITEMS**, que indica el final de la enumeración.

La [**función DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) enumerará los controladores de dominio en dos grupos. El primer grupo contiene los controladores de dominio que cubren el sitio del equipo donde se ejecuta la función y el segundo grupo contiene los controladores de dominio que no cubren el sitio del equipo donde se ejecuta la función. Si se especifica la marca **DS \_ NOTIFY AFTER \_ SITE \_ \_ RECORDS** en el parámetro *OptionFlags* en [**DsGetDcOpen,**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)la función **DsGetDcNext** devolverá **ERROR \_ FILEMARK \_ DETECTED** después de que se hayan recuperado todos los controladores de dominio específicos del sitio. **DsGetDcNext** comenzará a enumerar el segundo grupo, que contiene todos los controladores de dominio del dominio, incluidos los controladores de dominio específicos del sitio incluidos en el primer grupo.

Los controladores de dominio que controlan el sitio del equipo donde se ejecuta la función se enumeran primero seguidos de los controladores de dominio que no cubren el sitio del equipo donde se ejecuta la función. Se dice que un controlador de dominio cubre un sitio si el controlador de dominio está configurado para residir en ese sitio o si el controlador de dominio reside en un sitio más cercano al sitio en cuestión en términos del costo del vínculo entre sitios configurado. Si hay controladores de dominio en el grupo de controladores de dominio que cubren y el grupo de controladores de dominio que no cubren el sitio del equipo, los controladores de dominio se devuelven dentro del grupo en orden de sus prioridades y pesos configurados que se especifican en DNS. Los controladores de dominio que tienen una prioridad numérica inferior se devuelven primero dentro de un grupo. Si dentro de un grupo relacionado con el sitio hay un subgrupo de varios controladores de dominio con la misma prioridad, los controladores de dominio se devuelven en un orden aleatorio ponderado donde los controladores de dominio con mayor peso tienen más probabilidad de que se devuelvan primero. El administrador del dominio configura los sitios, prioridades y pesos para lograr un rendimiento y equilibrio de carga efectivos entre varios controladores de dominio disponibles en el dominio. Por este problema, las aplicaciones que usan las funciones [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) / [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) aprovechan automáticamente estas optimizaciones.

Cuando la enumeración está completa o ya no es necesaria, la enumeración debe cerrarse mediante una llamada a [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) con el identificador de contexto de enumeración de dominio.

Para restablecer la enumeración, es necesario cerrar la enumeración actual llamando a [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) y, a continuación, volver a abrir la enumeración llamando a [**DsGetDcOpen de**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) nuevo.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo usar estas funciones para enumerar los controladores de dominio en el dominio local.


```C++
DWORD dwRet;
PDOMAIN_CONTROLLER_INFO pdcInfo;

// Get a domain controller for the domain this computer is on.
dwRet = DsGetDcName(NULL, NULL, NULL, NULL, 0, &pdcInfo);
if(ERROR_SUCCESS == dwRet)
{
    HANDLE hGetDc;
    
    // Open the enumeration.
    dwRet = DsGetDcOpen(    pdcInfo->DomainName,
                            DS_NOTIFY_AFTER_SITE_RECORDS,
                            NULL,
                            NULL,
                            NULL,
                            0,
                            &hGetDc);
    if(ERROR_SUCCESS == dwRet)
    {
        LPTSTR pszDnsHostName;

        /*
        Enumerate each domain controller and print its name to the 
        debug window.
        */
        while(TRUE)
        {
            ULONG ulSocketCount;
            LPSOCKET_ADDRESS rgSocketAddresses;

            dwRet = DsGetDcNext(
                hGetDc, 
                &ulSocketCount, 
                &rgSocketAddresses, 
                &pszDnsHostName);
            
            if(ERROR_SUCCESS == dwRet)
            {
                OutputDebugString(pszDnsHostName);
                OutputDebugString(TEXT("\n"));
                
                // Free the allocated string.
                NetApiBufferFree(pszDnsHostName);

                // Free the socket address array.
                LocalFree(rgSocketAddresses);
            }
            else if(ERROR_NO_MORE_ITEMS == dwRet)
            {
                // The end of the list has been reached.
                break;
            }
            else if(ERROR_FILEMARK_DETECTED == dwRet)
            {
                /*
                DS_NOTIFY_AFTER_SITE_RECORDS was specified in 
                DsGetDcOpen and the end of the site-specific 
                records was reached.
                */
                OutputDebugString(
                  TEXT("End of site-specific domain controllers\n"));
                continue;
            }
            else
            {
                // Some other error occurred.
                break;
            }
        }
        
        // Close the enumeration.
        DsGetDcClose(hGetDc);
    }
    
    // Free the DOMAIN_CONTROLLER_INFO structure. 
    NetApiBufferFree(pdcInfo);
}
```



 

 




