---
title: Funciones ADSI
description: Active Directory interfaces de servicio exponen las siguientes funciones auxiliares a los clientes que no usan la automatización.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, referencia, funciones
- ADSI de la función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356714"
---
# <a name="adsi-functions"></a>Funciones ADSI

Active Directory interfaces de servicio exponen las siguientes funciones auxiliares a los clientes que no usan la automatización.



| Función                                           | Descripción                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | Crea un objeto enumerador para el objeto contenedor ADSI especificado.                              |
| [**ADsBuildVarArrayInt**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | Compila una matriz de tipo Variant a partir de una matriz de **DWORD** s.                                                |
| [**ADsBuildVarArrayStr**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | Compila una matriz de tipo Variant a partir de una matriz de cadenas Unicode.                                           |
| [**ADsEncodeBinaryData**](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | Convierte un BLOB de datos binarios en el formato adecuado para un filtro de búsqueda.                         |
| [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | Rellena una matriz de tipo Variant con elementos recuperados del objeto de enumerador especificado.            |
| [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | Libera un objeto de enumerador creado previamente por [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator). |
| [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | Recupera el último valor de código de error del subproceso que realiza la llamada.                                         |
| [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | Enlaza a un objeto ADSI con las credenciales actuales.                                             |
| [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | Enlaza a un objeto ADSI mediante las credenciales especificadas                                                |
| [**ADsSetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | Establece el valor del código de error del subproceso que realiza la llamada.                                                   |
| [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | Asigna un bloque de memoria.                                                                       |
| [**AllocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | Asigna memoria para una cadena determinada.                                                               |
| [**FreeADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | Libera la memoria asignada por [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).                                  |
| [**FreeADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | Libera la memoria asignada para la cadena especificada.                                                   |
| [**ReallocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | Asigna el contenido de la memoria existente a una ubicación de memoria recién creada.                            |
| [**ReallocADsStr**](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | Reemplaza una cadena existente por otra nueva.                                                        |



 

Las siguientes funciones ADSI están obsoletas.



| Función                                                  | Descripción |
|-----------------------------------------------------------|-------------|
| [**AdsFreeAllErrorRecords**](obsolete-adsi-functions.md) | Obsoleto.   |
| [**AdsDecodeBinaryData**](obsolete-adsi-functions.md)    | Obsoleto.   |
| [**PropVariantToAdsType**](obsolete-adsi-functions.md)   | Obsoleto.   |
| [**AdsTypeToPropVariant**](obsolete-adsi-functions.md)   | Obsoleto.   |
| [**AdsFreeAdsValues**](obsolete-adsi-functions.md)       | Obsoleto.   |
| [**InitAdsMem**](obsolete-adsi-functions.md)             | Obsoleto.   |
| [**AssertAdsmemLeaks**](obsolete-adsi-functions.md)      | Obsoleto.   |
| [**DumpMemorytracker**](obsolete-adsi-functions.md)      | Obsoleto.   |



 

 

 




