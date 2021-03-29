---
title: Enumerar controladores de dominio
description: En versiones anteriores de Windows, una aplicación solo podía obtener un único controlador de dominio en un dominio llamando a DsGetDcName.
ms.assetid: bfc92777-6944-406a-8b93-949a1cf3e2c3
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, enumerar controladores de dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94384bb8c62edb7b0d45328dabe7765a43e4e610
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773231"
---
# <a name="enumerating-domain-controllers"></a>Enumerar controladores de dominio

En versiones anteriores de Windows, una aplicación solo podía obtener un único controlador de dominio en un dominio llamando a [**DsGetDcName**](/windows/desktop/api/DsGetDC/nf-dsgetdc-dsgetdcnamea). No había forma de predecir qué controlador de dominio se recuperaría o para obtener una lista de los controladores de dominio. Windows permite a una aplicación enumerar los controladores de dominio de un dominio mediante las funciones [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta)y [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Para enumerar un controlador de dominio, llame a [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena). Esta función toma parámetros que definen el dominio que se va a enumerar y otras opciones de enumeración. **DsGetDcOpen** proporciona un identificador de contexto de enumeración de dominio que se usa para identificar la operación de enumeración cuando se llama a [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) y [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) .

Se llama a la función [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) con el identificador de contexto de enumeración de dominio para recuperar el siguiente controlador de dominio en la enumeración. La primera vez que se llama a esta función, se recupera el primer controlador de dominio de la enumeración. La segunda vez que se llama a esta función, se recupera el segundo controlador de dominio de la enumeración. Este proceso se repite hasta que **DsGetDcNext** devuelve el **error \_ no \_ más \_ elementos**, que indica el final de la enumeración.

La función [**DsGetDcNext**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) enumerará los controladores de dominio en dos grupos. El primer grupo contiene los controladores de dominio que cubren el sitio del equipo en el que se ejecuta la función y el segundo grupo contiene los controladores de dominio que no cubren el sitio del equipo en el que se ejecuta la función. Si se especifica la marca **DS \_ Notify \_ After \_ \_ Records site** en el parámetro *OptionFlags* de [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena), la función **DsGetDcNext** devolverá una marca de tiempo de **error \_ \_ detectada** después de que se hayan recuperado todos los controladores de dominio específicos del sitio. **DsGetDcNext** comenzará a enumerar el segundo grupo, que contiene todos los controladores de dominio del dominio, incluidos los controladores de dominio específicos del sitio contenidos en el primer grupo.

Los controladores de dominio que administran el sitio del equipo en el que se ejecuta la función se enumeran primero seguidos de los controladores de dominio que no cubren el sitio del equipo en el que se ejecuta la función. Se dice que un controlador de dominio cubre un sitio si el controlador de dominio está configurado para residir en ese sitio o si el controlador de dominio reside en un sitio más cercano al sitio en cuestión en lo que respecta al costo de vínculo configurado entre sitios. Si hay controladores de dominio en el grupo de controladores de dominio que cubren y el grupo de controladores de dominio que no cubren el sitio del equipo, se devuelven controladores de dominio en el grupo en el orden de las prioridades y pesos configurados que se especifican en DNS. Los controladores de dominio que tienen una prioridad numérica más baja se devuelven primero dentro de un grupo. Si en un grupo relacionado con el sitio hay un subgrupo de varios controladores de dominio con la misma prioridad, los controladores de dominio se devuelven en un orden aleatorio ponderado, donde los controladores de dominio con mayor peso tienen más probabilidad de ser devueltos en primer lugar. El administrador del dominio configura los sitios, las prioridades y los pesos para lograr un rendimiento eficaz y un equilibrio de carga entre varios controladores de dominio disponibles en el dominio. Por este motivo, las aplicaciones que usan [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena)las / [](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcnexta) / funciones [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) de DsGetDcNext de DsGetDcOpen aprovechan automáticamente estas optimizaciones.

Cuando la enumeración está completa o ya no es necesaria, la enumeración debe cerrarse llamando a [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) con el identificador de contexto de enumeración de dominio.

Para restablecer la enumeración, es necesario cerrar la enumeración actual llamando a [**DsGetDcClose**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcclosew) y, a continuación, volver a abrir la enumeración llamando a [**DsGetDcOpen**](/windows/desktop/api/Dsgetdc/nf-dsgetdc-dsgetdcopena) de nuevo.

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo usar estas funciones para enumerar los controladores de dominio del dominio local.


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



 

 




